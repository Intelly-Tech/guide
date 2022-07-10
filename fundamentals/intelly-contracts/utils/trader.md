---
description: A Smart Contract for Listing Intelly Assets (INFT) and Investing operation.
---

# Trader

{% hint style="info" %}
**Intelly: Trader** interacts with **Intelly: Access** for role management, **Intelly: Estate** (**INFT**) for invest operation and **Intelly: Token** (**INTL**) to receive payments with **Intelly: Oracle** price feeder.
{% endhint %}

## Contract info

**Contract name:** Trader

**Contract address:** 0x5dc28C48f2800E8ED9ca2193e5B1D46e7778AbA9



View [Trader.sol](https://github.com/intelly-dev/contracts/blob/main/contracts/utils/Trader.sol) on GitHub

View [Intelly: Trader contract on BscScan](https://testnet.bscscan.com/address/0x5dc28C48f2800E8ED9ca2193e5B1D46e7778AbA9) (Sample)

## Read functions

### **GETTERS**

{% tabs %}
{% tab title="access" %}
`function access() public view returns (address);`
{% endtab %}

{% tab title="admin" %}
`function admin() public view returns (bytes32);`
{% endtab %}

{% tab title="oracle" %}
`function oracle() public view returns (bytes32);`
{% endtab %}

{% tab title="stable" %}
`function stable() public view returns (bytes32);`
{% endtab %}

{% tab title="token" %}
`function token() public view returns (bytes32);`
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Returns the **`address` ** of contracts used on **`Intelly Trader`**.
{% endhint %}

### **listings**

`function getListing(address contract, uint256 tokenId) public view returns (Listing memory);`

{% hint style="info" %}
Returns predefined struct type **Listing** with a single piece of fraction **price** and the **creator** of listed INFT **contract** on **`Intelly Trader`**.
{% endhint %}

## Write functions

### **SETTERS**

{% tabs %}
{% tab title="setAccess" %}
`function setAccess() public view returns (address);`
{% endtab %}

{% tab title="setAdmin" %}
`function setAdmin(address _admin) public onlyRole(OPERATOR_ROLE);`
{% endtab %}

{% tab title="setOracle" %}
`function setOracle(address _oracle) public onlyRole(OPERATOR_ROLE);`
{% endtab %}

{% tab title="setStable" %}
`function setStable(address _stable) public onlyRole(OPERATOR_ROLE);`
{% endtab %}

{% tab title="setToken" %}
`function setToken(address _token) public onlyRole(OPERATOR_ROLE);`
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Sets the **`address` ** of contracts used on **`Intelly Trader`**.
{% endhint %}

### list

`function list(address creator, address inft, uint id, uint price);`

{% hint style="info" %}
Adds **approved** Intelly Estate (**INFT**) to **listings** mapping for investment.
{% endhint %}

### purchase

`function purchase(address inft, uint id, uint amount);`

{% hint style="info" %}
Purchases the specified **amount** Intelly Assets (**INFT**) fraction(s) by paying with Intelly Token (**INTL)**.
{% endhint %}

