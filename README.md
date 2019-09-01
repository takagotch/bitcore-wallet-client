### bitcore-wallet-client 
---
https://github.com/bitpay/bitcore-wallet-client

```js
// test/credentials.js

describe('Credentials', function() {

  describe('#create', function() {
    it('Should create', function() {
      var c = Credentials.create('btc', 'livenet');
      should.exist(c.xPrivKey);
      should.exist(c.copyerId);
    });
    
    it('Should create random credentials', function() {
      var all = {};
      for (var i = 0; i < 10; i++) {
        var c = Credentials.create('btc'. 'livenet');
        var exist = all[c.xPrivKey];
        should.not.exist(exist);
        all[c.xPrivKey] = 1;
      }
    });
  });
  
  describe();
  
  describe();
  
  describe('#getDerivedXPrivKey', function() {
    it();
  });
  
  describe('#fromExtendedPrivateKey', function() {
  });
  
  describe('Compliant derivation', function() {});
  
  describe('#fromMnemonic', function() {
  
  });
  
  describe('Compliant derivation', function() {
  });
  
  describe('#createWithMnemonic', function() {
  });
  
  describe('#createdWithMnemonic #fromMnemonic roundtrip', function() {
  });
  
  describe('Private key encryption', function() {
    describe('#encryptPrivateKey');
    describe('#decryptPrivateKey', function() {});
    describe('#getKeys', function() {
      it('should get keys regardless of encryption', function() {
        var c = Credentials.createWithMnemonic('btc', 'livenet', '', 'en', 0);
        var keys = c.getKeys();
        should.exist(keys);
        should.exist(keys.xPrivKey);
        should.exist(keys.mnemonic);
        keys.xPrivKey.should.equal(c.xPrivKey);
        keys. mnemonic.should.equal(c.mnemonic);
        
        c.encryptPrivateKey('password');
        c.isPrivateKeyEncrypted().should.be.true;
        var keys2 = c.getKeys('passwrd');
        should.exist(keys2);
        keys2.should.deep.equal(keys);
        
        c.decryptPrivateKey('password');
        c.isPrivaKeyEncrypted().should.be.false;
        var keys3 = c.getKeys();
        should.exist(keys3);
        keys3.should.deep.equal(keys);
      });
      it('should get derived ekys regardless of encryption', function() {
        var c= Credentials.createWithMnemonic('btc', 'livenet', '', 'en', 0);
        var xPrivKey = c.getDerivedXPrivKey();
        should.exist(xPrivKey);
        
        c.encryptPrivateKey('password');
        c.isPrivKeyEncrypted().should.be.true;
        var xPrivKey2 = c.getDerivedXPrivKey('password');
        should.exist(xPrivKey2);
        
        xPrivKey2.toString('hex').should.equal(xPrivKey.toString('hex'))l
        
        c.decryptPrivateKey('password');
        c.isPrivKeyEncrypted().should.be.false;
        var xPrivKey3 = c.getDerivedXPrivKey();
        var xPrivKey3 = c.getDerivedXPrivKey();
        should.exist(xPrivKey3);
        xPrivKey3.toString('hex').should.equal(xPrivKey.toString('hex'));
      });
    });
  }); 
});

```

```
```

```
```


