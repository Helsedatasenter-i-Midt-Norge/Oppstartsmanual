# Conquest DICOM Server

_En svært konfigurerbart, bildearkiverings- og kommunikasjonssystem (PACS)_

### Innstillinger

De fleste innstillingene kan endres i fanen «Configuration» i Conquest Windows-appen. Ytterligere innstillinger finner du i filen c:\dicomserver\dicom.ini, men disse vil tilbakestilles til standard [...]

Som standard mottas de innkommende filene i S:\dicomserver\Data\incoming, og lagres i S:\dicomserver\Data\.

Filer kan blas gjennom i selve Conquest-appen, eller det er mulig å koble til lokalserveren via, for eksempel:
- 3D Slicer
- Python (bruk pynetdicom)
- R (bruk DCMTK eller dcm4che)

Koble til følgende
- Server IP - 127.0.0.1 eller localhost
- DICOM port - 5678
- Conquest AE title - CONQUESTSRV1

### Dokumentasjon

- [Brukermanualen](https://github.com/marcelvanherk/Conquest-DICOM-Server/blob/master/windowsmanual.pdf)



_Sist oppdatert: 2026-06-30_
