# Backup do Firmware para BY Tech Gaming Keyboard

Este repositório contém uma cópia de backup do firmware para o teclado BY Tech Gaming Keyboard. Este firmware foi obtido e é distribuído sob a GNU General Public License v2.0.

## Descrição do Modelo

- **Modelo**: K624P - Redragon Elise Pro
- **Número de Série**: RD-K624P-KRS
- **Código do Produto**: RD-K624P-KRS
- **Entrada de Carga**: 5V = 1A
- **Fabricação**: Feito na China

Este firmware é especificamente para o modelo acima mencionado e foi criado usando a `sinowealth-kb-tool`, desenvolvida por carlossless. Esta ferramenta é uma aplicação de código aberto destinada a manipular dispositivos baseados em Sinowealth 8051.

## Pré-requisitos

Antes de proceder com o backup ou a restauração do firmware, certifique-se de que você tem:

- Um sistema Linux (testado no Linux Mint 20.2).
- Instalado Rust e Cargo para rodar a `sinowealth-kb-tool`.
- Permissões adequadas configuradas no sistema para acessar o teclado via USB.

## Instalação da Ferramenta

Para instalar a `sinowealth-kb-tool`, você pode seguir os seguintes passos:

```bash
# Instale Rust e Cargo, se ainda não estiver instalado
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

# Instale a sinowealth-kb-tool usando Cargo
cargo install sinowealth-kb-tool
```

## Usando o Firmware

### Backup do Firmware

Para fazer um backup do firmware do seu teclado, execute o seguinte comando:

```bash
sinowealth-kb-tool read --vendor_id 0x258a --product_id 0x0049 --firmware_size 61440 --bootloader_size 4096 --page_size 2048 --isp_iface_num 1 --isp_usage_page 0xff00 --isp_usage 0x0001 --isp_index 0 --reboot false /path/to/your/backup_file.hex
```

### Restauração do Firmware

Para restaurar ou escrever o firmware no teclado:

```bash
sinowealth-kb-tool write --vendor_id 0x258a --product_id 0x0049 --firmware_size 61440 --bootloader_size 4096 --page_size 2048 --isp_iface_num 1 --isp_usage_page 0xff00 --isp_usage 0x0001 --isp_index 0 --reboot true /path/to/your/backup_file.hex
```

## Aviso Legal

Este firmware é fornecido "como está", sem garantias de qualquer tipo, expressas ou implícitas. O uso deste firmware é por sua conta e risco. Não sou responsável por quaisquer danos que possam ocorrer devido ao uso deste firmware.

## Contribuindo

Se você encontrou um bug ou tem melhorias para sugerir, sinta-se à vontade para criar um issue ou enviar um pull request.

## Licença

Este projeto está licenciado sob a GNU General Public License v2.0. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## Agradecimentos

Gostaria de expressar minha gratidão a algumas pessoas incríveis que me ajudaram a tornar este projeto possível:

- **Sherman729**: Um grande obrigado ao Sherman729 no Discord, que não apenas me apresentou a `sinowealth-kb-tool`, mas também me tranquilizou sobre seu uso. Suas orientações foram essenciais para me ajudar a navegar pelo processo de backup e restauração do firmware do meu teclado.

- **Karolis Stasaitis (carlossless)**: Um agradecimento a Karolis Stasaitis , o desenvolvedor por trás da [sinowealth-kb-tool](https://github.com/carlossless/sinowealth-kb-tool). Sua ferramenta abriu novas possibilidades para usuários de teclados Sinowealth, permitindo uma personalização e manutenção significativas do hardware. Sua contribuição para a comunidade é verdadeiramente valiosa.

Seu trabalho e apoio não apenas facilitaram este projeto, mas também ajudaram a fortalecer a comunidade que depende dessas ferramentas para melhorar e personalizar seus dispositivos.


---

Here is the final version of your README in English, polished and ready to be used in your GitHub repository:

---
**ENGLISH VERSION**

# Firmware Backup for BY Tech Gaming Keyboard

This repository contains a backup copy of the firmware for the BY Tech Gaming Keyboard. This firmware was obtained and is distributed under the GNU General Public License v2.0.

## Model Description

- **Model**: K624P - Redragon Elise Pro
- **Serial Number**: RD-K624P-KRS
- **Product Code**: RD-K624P-KRS
- **Power Input**: 5V = 1A
- **Manufactured in**: China

This firmware is specifically for the above-mentioned model and was created using the `sinowealth-kb-tool`, developed by carlossless. This tool is an open-source application designed to manipulate devices based on the Sinowealth 8051.

## Prerequisites

Before proceeding with the firmware backup or restoration, ensure that you have:

- A Linux system (tested on Linux Mint 20.2).
- Rust and Cargo installed to run the `sinowealth-kb-tool`.
- Proper permissions configured on the system to access the keyboard via USB.

## Tool Installation

To install the `sinowealth-kb-tool`, you can follow these steps:

```bash
# Install Rust and Cargo if not already installed
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

# Install the sinowealth-kb-tool using Cargo
cargo install sinowealth-kb-tool
```

## Using the Firmware

### Firmware Backup

To back up the firmware of your keyboard, execute the following command:

```bash
sinowealth-kb-tool read --vendor_id 0x258a --product_id 0x0049 --firmware_size 61440 --bootloader_size 4096 --page_size 2048 --isp_iface_num 1 --isp_usage_page 0xff00 --isp_usage 0x0001 --isp_index 0 --reboot false /path/to/your/backup_file.hex
```

### Firmware Restoration

To restore or write the firmware to the keyboard:

```bash
sinowealth-kb-tool write --vendor_id 0x258a --product_id 0x0049 --firmware_size 61440 --bootloader_size 4096 --page_size 2048 --isp_iface_num 1 --isp_usage_page 0xff00 --isp_usage 0x0001 --isp_index 0 --reboot true /path/to/your/backup_file.hex
```

## Disclaimer

This firmware is provided "as is", without any kind of warranties, express or implied. Use of this firmware is at your own risk. I am not responsible for any damages that may occur due to the use of this firmware.

## Contributing

If you have found a bug or have suggestions for improvements, feel free to create an issue or send a pull request.

## License

This project is licensed under the GNU General Public License v2.0. See the [LICENSE](LICENSE) file for more details.

## Acknowledgements

I would like to express my gratitude to some amazing individuals who helped make this project possible:

- **Sherman729**: A huge thank you to Sherman729 on Discord, who not only introduced me to the `sinowealth-kb-tool` but also reassured me about its use. His guidance was crucial in helping me navigate the process of backing up and restoring my keyboard's firmware.

- **Karolis Stasaitis (carlossless)**: Special thanks to Karolis Stasaitis, the developer behind the [sinowealth-kb-tool](https://github.com/carlossless/sinowealth-kb-tool). His tool has opened new possibilities for Sinowealth keyboard users, allowing significant customization and maintenance of hardware. His contributions to the community are truly invaluable.

Their work and support not only facilitated this project but also helped strengthen the community that relies on these tools to enhance and personalize their devices.



