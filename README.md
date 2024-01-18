# ⚛️ Offline Pix RFC
RFC describing the "Offline Pix" feature architecture, focused on providing easy-to-use offline pix payments based on QRCodes in a safe way with security constraints and expiration time.

## Summary

- Problem description
- Personas
- Usability
- Security
- Profitability

## Problem description

PIX is a great way to transfer money in Brazil, it comes with a great architecture that provides reliability, speed and practicity to transfer money to anyone who has an account to a service that is integrated to the BACEN (Banco Central) api. Besides that, the technology relies too much on internet availability and that can be a problem in regions where the internet is limited or not present at all and also situations where the receiver has access to the internet but the payer don't. This solution focus on a two-way product that aims to solve these problems by providing a reliable, secure and high-customizable method to transfer money through pix, using QR Codes.

## Personas

- *emitter* of a offline PIX QRCode
- *receivers* of a offline PIX QRCode
- *intermediator* of the transactions

<br>

- The **emitter** is the person that will use the application/webserver to emit the QRCode to be used offline.
- The **receivers** is the group of people that will receive transactions using the QRCode provided by the **emitter**
- The **intermediator** is the application/webserver that is providing the entire feature

> [!IMPORTANT]  
> The **intermediator** must control an account possessed by the **emitter** in order to automatically schedule
> and send PIX transactions to the **receivers**, otherwise a manual action will be needed, defeating the purpose of
> providing offline transactions.
