
# Azure VMs

- Azure VMs är väldigt konfigurerbara servrar.
- Helt utan att hantera fysisk hårdvara
- Storleken bestäms utav din Azure image, som definierar din kombination av cpu, minne och lagring.
- Prissättning gäller per timme
- Upptid på 99.9 med en instans och 99.95 med två instanser (availability set)
- Finns en mobilapp för att enklet övervaka VMs
- Stöd för både windows och linux
- Du har ansvar för patchning av OS osv. (MJUKVARA)


Vid skapande av en vm, skapas/associeras också:
- Network Security Group (NSG)
	- Virtuell brandvägg med regler och protokoll, kopplad till NIC.
- Network Interface (NIC)
	- Tar hand om ip protokoll och kommunikation med internet
- VM instance
	- Din server
- Virtual Network (Vnet)
	- Privata nätverket för din VM
- Public IP
	- Publik adress för att anslutning

##### Azure Compute Units

 - Är ett värde för att jämföra skillnader mellan alla computes på Azure SKUs (prisgrupper)
- ACU standard är mätt från small(standard-A1) som värdet 100

##### Storlekar/typer av VMs
-  General Purpose
	- Balanserad CPU till minne
  	- Bäst för test, utveckling, små/medium databaser och lågt trafikerade webbtjänster
  	- SKUs: B, Dsv3, Dasv4, DSv2, Dv2, Av2, Dc, DCv2, Dv4, Dsv4, Ddv4, Ddsv4
  
- Compute Optimized
	- Hög CPU till minne
	- Bäst för webbtjänster med medium trafik
	- SKUs: F,Fs,Fsv2

- Memory Optimized
	- Hög minne till CPU
	- Bäst för relationsdatabas servrar, medium till stora caches
	- SKUs: Esv3, Ev3, Easv4, Ev4, Eav4, Esv4, Edsv4, Mv2, M, DSv2, Dv2

- Storage Optimized
	- Hög diskläsningshastighet och IO
	- Bäst för big data, SQL och NoSql databaser, data warehouseing
	- SKUs: Lsv2

- GPU
	- Specialiserade VMs för grafikrendering
	- Bäst för Videoredigering, modell träning, depp learning osv
	- SKUs: NC, NCv2, NCv3, NCasT4_v3, ND, NDv2, NVv3, NVv4

- High performance compute
	- Snabbaste Azure erbjuder,  hög CPU med tillval på nätverks delen
	- SKUs: HB,HBv2, HC, H

##### Hyper-V gen 1 och gen 2 (Hardware virtualization product)
-  Gen 1
	- BIOS baserad arkitektur
- Gen 2
	- UEFI baserad arkitektur
	- Secure boot stöd
	- Stöd för större operativsystem


##### SSH, RDP och Bastions (Ansluta till VMs)
- SSH - Secure Shell (terminal) , via port 22 och TCP ofta med RSA Key pairs för autentisering.
- RDP - Remote Desktop Protocol - Grafiskt gränssnitt för att ansluta utvecklat av Microsoft, via port 3389 och TCP/UDP
- Bastions - En service för att ansluta till VMs via webbläsaren och Azure portalen.


### VMs Cheat Sheet
<img width="1796" height="885" alt="Skärmbild 2025-12-14 193907" src="https://github.com/user-attachments/assets/3d42b83a-325e-4053-b747-303cf26389a6" />
<img width="1892" height="575" alt="Skärmbild 2025-12-14 193934" src="https://github.com/user-attachments/assets/1d503080-2b3a-4440-b046-c4cec5a0f7c2" />


