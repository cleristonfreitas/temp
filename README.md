# temp


será apagado

O LLMNR (Link-Local Multicast Name Resolution) e o NBT-NS (Netbios Name Service) são dois protocolos do Windows que funcionam como alternativas ao protocolo DNS (Domain Name System).

Uma maquina Windows segue algumas etapas quando precisa resolver um nome de domínio.

1- Tenta a resolução arquivo arquivo hosts local;
2- Tenta a resoluçção através do cache do DNS;
3- Envia a solicitação para servidor DNS para resolução;
4- A solicitação é enviada para os protocolos LLMNR e NBT-NS

O LLMNR e o NBT-NS resolvem nomes através de consultas enviadas em broadcast para todas as máquinas da rede local. Se uma máquina conhecer o nome solicitado, ela responderá à consulta. 

A vulnerabilidade ocorre quando a máquina atacante solicita um desafio à máquina vitimada, que inclui o envio do nome de usuário e o hash NTLM da senha. O hash NTLM é um valor criptografado usado para autenticação em sistemas Windows. O atacante pode tentar quebrar esse hash para obter a senha em texto claro ou usar o hash em técnicas como Pass-the-Hash.
