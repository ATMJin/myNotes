---
date: 2022-06-10
aliases: []
---

# S.O.L.I.D 原則

為了開發出高內聚、低耦合的系統以提高維護性，所依循的原則。

## Single-responsibility principle (SRP) 單一職責原則

> “A class should have only one reason to change.”

一個模組應有且只有一個理由會使其改變。
一個模組應只對唯一的一個角色負責

## Open–closed principle (OCP) 開放封閉原則

> "You should be able to extend the behavior of a system without having to modify that system."

一個軟體製品在面對擴展時是開放的，且擴充時不應修改到原有的程式。

## Liskov substitution principle (LSP) 里氏替換原則

> 若對型態 S 的每一個物件 o1，都存在一個型態為 T 的物件 o2，使得在所有針對 T 編寫的程式 P 中，用 o1 替換 o2 後，程式 P 的行為功能不變，則 S 是 T 的子型態。
> T(o2) <-- P 針對 T 編寫的程式 P 中
> S(o1) <-- P 用 o1 替換 o2 後，程式 P 的行為功能不變
> T(o2) <-- S(o1) S 是 T 的子型態

子型態必須遵從父型態的行為進行設計。

## Interface segregation principle (ISP) 介面隔離原則

> No client should be forced to depend on methods it does not use.

模組與模組之間的依賴，不應有用不到的功能可以被對方呼叫。

## Dependency inversion principle (DIP) 依賴反向原則

> 高層模組不應依賴低層模組，它們都應依賴於抽象介面。抽象介面不應該依賴於具體實作，具體實作應依賴抽象介面。

低層模組：該模組的實現都是不可分割的原子邏輯層，如 MVC 中的 Model 層。
高層模組：該模組的業務邏輯多是由低層模組組合而成，如 MVC 中的 Controller 層與 Client 端。
