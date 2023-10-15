# Burlando o BootSecureCheck do Windows 11 
    Na tela de instalação, onde aparece a mensagem que não é possível instalar o Windows 11
        Pressione juntas as teclas "SHIFT" + "F10"
        Aparecerá o prompt do Windows
            Digite:
                regedit.exe
            Dentro o Regedit faça o seguinte caminho:
                HKEY_LOCAL_MACHINE >> SYSTEM >> SETUP
                    Clique com botão direito sobre "SETUP" e no menu que aparecer escolha "Chave"
                    Será criada uma nova pasta na hierarquia dentro do SETUP
                        Coloque o nome: LabConfig
                        Selecione a chave ou pasta LabConfig e no painel da direita crie dois registro do tipo "Valor DWORD (32 bits)"
                        Nomeie-os da seguinte forma: O primeiro com o nome "BypassTPMCheck" e o outro "BypassSecureBootCheck"
                        >>>>> Em ambos clique duas vezes e altere o valor para 1 

                    Feche o regedit
                    Feche o prompt
                    Na tela de instalação, clique em voltar e depois avance para continuar a instalação novamente.
                    
                    Se pedir para criar conta Microsoft, vc tem duas opções:
                    1) Apertar "SHIFT" + "F10" e no prompt digitar taskmgr.exe e encerre o aplicativo "sem rede". Depois feche o promt e clique em avançar;
                    2) Caso aparece a tela para criar a conta e o processo 1 não tenha dado certo, coloque os seguintes dados para criar a conta: test@test.com e senha: test
                       Depois é só clicar em avançar. 


Referência: https://www.youtube.com/watch?v=hd1Jkc50ji4