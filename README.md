
# UIAPduino対応 CP2102N搭載 小型USBシリアル変換モジュール

[日本語](README.md) | [English](README_EN.md)

## 概要

<div class="image-row">
    <img src="https://github.com/bigbenbigben/Tiny-USB-Serial-Module/blob/main/Tiny-USB-Serial-Module_top.jpeg" width="240px">
    &nbsp;&nbsp;&nbsp;&nbsp;
    <img src="https://github.com/bigbenbigben/Tiny-USB-Serial-Module/blob/main/Tiny-USB-Serial-Module_bottom.jpeg" width="210px">
</div>

Silicon Labs社のCP2102Nを採用した、基板サイズ20mm×12mmの小型USBシリアル変換基板です。

USB Type-C接続、USBバスパワー動作に対応しており、TxD、RxDはスルーホール端子から引き出しています。

<img src="https://github.com/bigbenbigben/Tiny-USB-Serial-Module/blob/main/Tiny-USB-Serial-Module_with_UIAPduino.jpeg" width="240px">

<img src="https://github.com/bigbenbigben/Tiny-USB-Serial-Module/blob/main/Tiny-USB-Serial-Module_with_UIAPduino_description.jpeg" width="640px">

本基板は[UIAPduino Pro Micro CH32V003 V1.4](https://www.uiap.jp/uiapduino/pro-micro/ch32v003/v1dot4)のピン配置に対応しており、コンスルーやブレッドボードによりRXD、TXD、GNDをそのまま接続することができます。

## サイズ

<img src="https://github.com/bigbenbigben/Tiny-USB-Serial-Module/blob/main/Tiny-USB-Serial-Module_size.jpeg" width="240px">

高さ：5mm（実測値）

## 特徴

- 小型です。（基板サイズ20mm×12mm）
- Silicon Labs社のCP2102Nを使用。
- 過電流保護回路搭載。
- 静電気対策回路搭載。
- USB Type-Cコネクタ搭載。
- USBバスパワー動作。
- 入力5Vトレラント。
- UIAPduinoにそのまま挿入できるピン配置になっています。
- RoHS対応です。

## 主な仕様

- 電源電圧Max.：5V
- IO電圧Max.：3.3V（入力5Vトレラント）
- ボーレートMin.：300bps
- ボーレートMax.：3Mbps
- 受信バッファ：512バイト
- 送信バッファ：512バイト
- LED 2個（電源：青、TxD：オレンジ）

## ピン配置

<img src="https://github.com/bigbenbigben/Tiny-USB-Serial-Module/blob/main/Tiny-USB-Serial-Module_pin.jpeg" width="240px">

- p1 ： +5V(VBUS)
- p2 ： RXD
- p3 ： TXD
- p4 ： GND

## 対応OS

本製品に使用しているCP2102Nは以下のOS向けにドライバが提供されています。

対象OS：Windows, macOS, Linux, and Android

ドライバ提供サイト：[https://www.silabs.com/software-and-tools/usb-to-uart-bridge-vcp-drivers?tab=downloads](https://www.silabs.com/software-and-tools/usb-to-uart-bridge-vcp-drivers?tab=downloads)

筆者は Windows 11 Pro 25H2 で動作を確認しています。

## 注意

- RXDは5V入力対応、TXDは3.3V出力です。一般的な5Vマイコンでは問題なく使用できますが、5Vロジック入力を必須とする機器には対応していません。
- TXD/RXDの接続には注意してください。例としてUART接続では、TXDとRXDをクロス接続します。本製品のTXDを相手機器のRXDへ、本製品のRXDを相手機器のTXDへ接続してください。
- 2026/7/12現在、UIAPduinoは`Serial.available()`が動かないようです。筆者は[UIAPSerial](https://github.com/tarosay/sdlog_uiapduino/tree/main/SDLog)というライブラリで動作確認しました。

## Author

ポジティブフィードバック
bigben (@bigbenbigben)
