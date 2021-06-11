---
title: Constantes MAPI
manager: soliver
ms.date: 10/02/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: Définitions des constantes, déclarations d’interface MAPI et identificateurs de classe et d’interface utilisés par les API MAPI.
ms.openlocfilehash: 343b777550d88276a1f5cad19f12ae7fc09c6244
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318920"
---
# <a name="mapi-constants"></a>Constantes MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique présente les définitions des constantes, les déclarations d’interface MAPI et les identificateurs de classe et d’interface utilisés par les API MAPI.
  
## <a name="class-and-interface-identifiers"></a>Identificateurs de classe et d’interface

Utilisez la macro DEFINE_GUID définie dans le fichier d’en-tête guiddef.h du kit de développement logiciel Windows (Kit SDK Windows) de Microsoft pour associer les noms symboliques de l’identificateur global unique (GUID) à leurs valeurs, sauf mention contraire.
  
## <a name="attachment-security-conversion-api"></a>API de conversion de sécurité des pièces jointes

Cette section contient les définitions des constantes et les identificateurs d’interface pour l’API de sécurité des pièces jointes.
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

Utilisez la macro MAPIMETHOD définie dans le fichier d’en-tête mapidefs.h du SDK Windows pour définir la fonction virtuelle pure **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**. 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

Utilisez la macro DECLARE_MAPI_INTERFACE_ définie dans le fichier d’en-tête mapidefs.h du SDK Windows pour définir le tableau de méthode virtuelle pour **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**. 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a>API de conversion MAPI-MIME

Cette section contient les définitions des constantes et les identificateurs de classe et d’interface pour l’API de conversion MAPI MIME.
  
### <a name="constants"></a>Constantes

|||
|:-----|:-----|
|CCSF_SMTP  <br/> |0x0002  <br/> |
|CCSF_NOHEADERS  <br/> |0x0004  <br/> |
|CCSF_USE_TNEF  <br/> | 0x0010  <br/> |
|CCSF_INCLUDE_BCC  <br/> |0x0020  <br/> |
|CCSF_8BITHEADERS  <br/> | 0x0040  <br/> |
|CCSF_USE_RTF  <br/> |0x0080  <br/> |
|CCSF_PLAIN_TEXT_ONLY  <br/> |0x1000  <br/> |
|CCSF_NO_MSGID  <br/> |0x4000  <br/> |
|CCSF_GLOBAL_MESSAGE  <br/> |0x00200000  <br/> |
|E_INVALIDARG  <br/> | *Comme définie dans le fichier d’en-tête winerror.h du kit de développement logiciel Windows (Kit SDK Windows) de Microsoft*  <br/> |
   
### <a name="class-identifiers"></a>Identificateurs de classe

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a>Identificateurs d’interface

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a>API de l’état hors connexion

Cette section contient les définitions des constantes et les identificateurs de classe et d’interface pour l’API de l’état hors connexion.
  
### <a name="constants"></a>Constantes

|||
|:-----|:-----|
|E_INVALIDARG  <br/> | *Comme définie dans le fichier d’en-tête winerror.h du kit de développement logiciel Windows (Kit SDK Windows) de Microsoft*  <br/> |
|E_NOINTERFACE  <br/> | *Comme définie dans le fichier d’en-tête winerror.h du kit de développement logiciel Windows (Kit SDK Windows)*  <br/> |
|MAPIOFFLINE_ADVISE_DEFAULT  <br/> |(ULONG)0  <br/> |
|MAPIOFFLINE_UNADVISE_DEFAULT  <br/> |(ULONG)0  <br/> |
|MAPIOFFLINE_ADVISE_TYPE_STATECHANGE  <br/> |1  <br/> |
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |0x1  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |0x2  <br/> |
|MAPIOFFLINE_FLAG_BLOCK  <br/> |0x00002000  <br/> |
|MAPIOFFLINE_FLAG_DEFAULT  <br/> |0x00000000  <br/> |
|MAPIOFFLINE_STATE_ALL  <br/> |0x003f037f  <br/> |
|**En ligne ou hors ligne** <br/> ||
|MAPIOFFLINE_STATE_OFFLINE_MASK  <br/> |0x00000003  <br/> |
|MAPIOFFLINE_STATE_OFFLINE  <br/> |0x00000001  <br/> |
|MAPIOFFLINE_STATE_ONLINE  <br/> |0x00000002  <br/> |
   
### <a name="class-identifiers"></a>Identificateurs de classe

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a>Identificateurs d’interface

```cpp
//{000672B5-0000-0000-c000-000000000046}
DEFINE_GUID(IID_IMAPIOffline, 0x000672B5, 0x0000, 0x0000, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
```

```cpp
//{0317bde5-fc29-44cd-8dcd-36125a3be9ec}
DEFINE_GUID(IID_IMAPIOfflineNotify, 0x0317bde5, 0xfc29, 0x44cd, 0x8d, 0xcd, 0x36, 0x12, 0x5a, 0x3b, 0xe9, 0xec);
```

```cpp
//{42175607-ff3e-4790-bc18-66c8643e6424
DEFINE_GUID(IID_IMAPIOfflineMgr, 0x42175607, 0xFF3E, 0x4790, 0xbc, 0x18, 0x66, 0xc8, 0x64, 0x3e, 0x64, 0x24);
```

## <a name="outlook-named-properties"></a>Propriétés nommées Outlook

Cette section contient les définitions des constantes des propriétés nommées et de leurs espaces de noms et d’autres constantes connexes.
  
### <a name="definitions-for-named-properties"></a>Définitions pour les propriétés nommées

```cpp
#define dispidMeetingType0x0026 
#define dispidFileUnder0x8005 
#define dispidYomiFirstName 0x802C 
#define dispidYomiLastName 0x802D 
#define dispidYomiCompanyName 0x802E 
#define dispidWorkAddressStreet 0x8045 
#define dispidWorkAddressCity 0x8046 
#define dispidWorkAddressState 0x8047 
#define dispidWorkAddressPostalCode 0x8048 
#define dispidWorkAddressCountry 0x8049 
#define dispidWorkAddressPostOfficeBox 0x804A 
#define dispidInstMsg 0x8062 
#define dispidEmailDisplayName 0x8080 
#define dispidEmailAddrType 0x8082 
#define dispidEmailEmailAddress 0x8083 
#define dispidEmailOriginalDisplayName 0x8084 
#define dispidEmail1OriginalEntryID0x8085 
#define dispidEmail2DisplayName 0x8090 
#define dispidEmail2AddrType 0x8092 
#define dispidEmail2EmailAddress 0x8093 
#define dispidEmail2OriginalDisplayName 0x8094 
#define dispidEmail2OriginalEntryID0x8095 
#define dispidEmail3DisplayName 0x80A0 
#define dispidEmail3AddrType 0x80A2 
#define dispidEmail3EmailAddress 0x80A3 
#define dispidEmail3OriginalDisplayName 0x80A4 
#define dispidEmail3OriginalEntryID0x80A5 
#define dispidTaskStatus 0x8101 
#define dispidTaskStartDate 0x8104 
#define dispidTaskDueDate 0x8105 
#define dispidTaskActualEffort 0x8110 
#define dispidTaskEstimatedEffort 0x8111 
#define dispidTaskFRecur 0x8126 
#define dispidBusyStatus0x8205 
#define dispidLocation 0x8208 
#define dispidApptStartWhole 0x820D 
#define dispidApptEndWhole 0x820E 
#define dispidApptDuration 0x8213 
#define dispidRecurring 0x8223 
#define dispidTimeZoneStruct0x8233 
#define dispidAllAttendeesString 0x8238 
#define dispidToAttendeesString 0x823B 
#define dispidCCAttendeesString 0x823C 
#define dispidConfCheck0x8240 
#define dispidApptCounterProposal 0x8257 
#define dispidApptTZDefStartDisplay0x825E 
#define dispidApptTZDefEndDisplay0x825F 
#define dispidApptTZDefRecur0x8260 
#define dispidReminderTime0x8502 
#define dispidReminderSet 0x8503 
#define dispidFormStorage0x850F 
#define dispidPageDirStream0x8513 
#define dispidSmartNoAttach 0x8514 
#define dispidCommonStart 0x8516 
#define dispidCommonEnd 0x8517 
#define dispidFormPropStream0x851B 
#define dispidRequest 0x8530 
#define dispidCompanies 0x8539 
#define dispidContacts0x853A 
#define dispidPropDefStream0x8540 
#define dispidScriptStream0x8541 
#define dispidCustomFlag0x8542 
#define dispidReminderNextTime 0x8560 
#define dispidHeaderItem0x8578 
#define dispidUseTNEF0x8582 
#define dispidToDoTitle0x85A4 
#define dispidLogType 0x8700 
#define dispidLogStart 0x8706 
#define dispidLogDuration 0x8707 
#define dispidLogEnd 0x8708 
```

### <a name="definitions-for-namespaces"></a>Définitions pour les espaces de noms

Les identificateurs globaux uniques (GUID) suivants représentent les espaces de noms des propriétés nommées.
  
```cpp
const GUID PS_INTERNET_HEADERS  = {0x00020386, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PS_PUBLIC_STRINGS    = {0x00020329, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Appointment= {0x00062002, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Address       = {0x00062004, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Common        = {0x00062008, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Log           = {0x0006200A, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Meeting = {0x6ED8DA90, 0x450B, 0x101B, {0x98, 0xDA, 0x00, 0xAA, 0x00, 0x3F, 0x13, 0x05}}; 
const GUID PSETID_Task          = {0x00062003, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
```

Consultez la section Banque MAPI pour obtenir les définitions PSETID.
  
### <a name="other-constants"></a>Autres constantes

|||
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0xD000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x2000000  <br/> |
|MNID_ID  <br/> | *Comme définie dans le fichier d’en-tête mapidefs.h.*  <br/> |
|MNID_STRING  <br/> | *Comme définie dans le fichier d’en-tête mapidefs.h.*  <br/> |
|mtgNone  <br/> |0x0  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |
|mtgFullUpdate  <br/> |0x00010000  <br/> |
|mtgInfoUpdate  <br/> |0x00020000  <br/> |
|mtgOutofDate  <br/> |0x00080000  <br/> |
|mtgDelegated  <br/> |0x00100000  <br/> |
   
## <a name="replication-api"></a>API de réplication

Cette section présente les définitions des constantes, les déclarations d’interface MAPI et les identificateurs de classe et d’interface de l’API de réplication.
  
### <a name="constants"></a>Constantes

Voici la structure d’une constante [MAPIUID](mapiuid.md) identifiant un fournisseur de services MAPI : 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|DNH_OK  <br/> |0x00010000  <br/> |
|DNT_OK  <br/> |0x00010000  <br/> |
|HSF_LOCAL  <br/> |0x00000008  <br/> |
|HSF_COPYDESTRUCTIVE  <br/> |0x00000010  <br/> |
|HSF_OK  <br/> |0x00010000  <br/> |
|MDB_OST_LOGON_UNICODE  <br/> |((ULONG) 0x00000800)  <br/> |
|MDB_OST_LOGON_ANSI  <br/> |((ULONG) 0x00001000)  <br/> |
|SHOW_SOFT_DELETES  <br/> |((ULONG) 0x00000002)  <br/> |
|SS_ACTIVE  <br/> |0  <br/> |
|SS_SUSPENDED  <br/> |1  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |
|SYNC_BACKGROUND  <br/> |0x00001000  <br/> |
|SYNC_THESE_FOLDERS  <br/> |0x00020000  <br/> |
|SYNC_HEADERS  <br/> |0x02000000  <br/> |
|UPC_OK  <br/> |0x00010000  <br/> |
|UPD_ASSOC  <br/> |0x00000001  <br/> |
|UPD_MOV  <br/> |0x00000002  <br/> |
|UPD_OK  <br/> |0x00010000  <br/> |
|UPD_MOVED  <br/> |0x00020000  <br/> |
|UPD_UPDATE  <br/> |0x00040000  <br/> |
|UPD_COMMIT  <br/> |0x00080000  <br/> |
|UPF_NEW  <br/> |0x00000001  <br/> |
|UPF_MOD_PARENT  <br/> |0x00000002  <br/> |
|UPF_MOD_PROPS  <br/> |0x00000004  <br/> |
|UPF_DEL  <br/> |0x00000008  <br/> |
|UPF_OK  <br/> |0x00010000  <br/> |
|UPH_OK  <br/> |0x00010000  <br/> |
|UPM_ASSOC  <br/> |0x00000001  <br/> |
|UPM_NEW  <br/> |0x00000002  <br/> |
|UPM_MOV  <br/> |0x00000004  <br/> |
|UPM_MOD_PROPS  <br/> |0x00000008  <br/> |
|UPM_HEADER  <br/> |0x00000010  <br/> |
|UPM_OK  <br/> |0x00010000  <br/> |
|UPM_MOVED  <br/> |0x00020000  <br/> |
|UPM_COMMIT  <br/> |0x00040000  <br/> |
|UPM_DELETE  <br/> |0x00080000  <br/> |
|UPM_SAVE  <br/> |0x00100000  <br/> |
|UPR_ASSOC  <br/> |0x00000001  <br/> |
|UPR_READ  <br/> |0x00000002  <br/> |
|UPR_OK  <br/> |0x00010000  <br/> |
|UPR_COMMIT  <br/> |0x00020000  <br/> |
|UPS_UPLOAD_ONLY  <br/> |0x00000001  <br/> |
|UPS_DNLOAD_ONLY  <br/> |0x00000002  <br/> |
|UPS_ONE_FOLDER  <br/> |0x00000004  <br/> |
|UPS_THESE_FOLDERS  <br/> |0x00000080  <br/> |
|UPS_OK  <br/> |0x00010000  <br/> |
|UPT_OK  <br/> |0x00010000  <br/> |
|UPT_PUBLIC  <br/> |0x00000001  <br/> |
|UPV_ERROR  <br/> |0x00010000  <br/> |
|UPV_DIRTY  <br/> |0x00020000  <br/> |
|UPV_COMMIT  <br/> |0x00040000  <br/> |
   
### <a name="interface-declarations"></a>Déclarations d’interface

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a>Identificateurs d’interface

```cpp
//{4FDEEFF0-0319-11CF-B4CF-00AA0DBBB6E6}
DEFINE_GUID (IID_IPSTX, 0x4FDEEFF0, 0x0319, 0x11CF, 0xB4, 0xCF, 0x00, 0xAA, 0x0D, 0xBB, 0xB6, 0xE6)
```

```cpp
//{2067A790-2A45-11D1-EB86-00A0C90DCA6D}
DEFINE_GUID (IID_IPSTX2, 0x2067A790, 0x2A45, 0x11D1, 0xEB, 0x86, 0x00, 0xA0, 0xC9, 0x0D, 0xCA, 0x6D)
```

```cpp
//{55f15320-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX3, 0x55f15320, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{aa2e2092-ac08-11d2-a2f9-0060b0ec3d4f}
DEFINE_GUID (IID_IPSTX4, 0xaa2e2092, 0xac08, 0x11d2, 0xa2, 0xf9, 0x00, 0x60, 0xb0, 0xec, 0x3d, 0x4f)
```

```cpp
//{55f15322-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX5, 0x55f15322, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{55f15323-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX6, 0x55f15323, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{d2d85db4-840f-49b8-9982-07d2405ec6b7}
DEFINE_GUID (IID_IOSTX, 0xd2d85db4,  0x840f, 0x49b8, 0x99, 0x82, 0x07, 0xd2, 0x40, 0x5e, 0xc6, 0xb7)
```

<br/>

Utilisez les deux identificateurs d’interface suivants avec [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir et ignorer les fournisseurs vérifiés sur un objet de dossier et un objet du message, respectivement. 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a>Banque MAPI

Cette section contient les définitions des constantes et les identificateurs d’interface utilisés par des API qui créent une interface avec une banque MAPI.
  
### <a name="constants"></a>Constantes

||||
|:-----|:-----|:-----|
|fnevIndexing  <br/> |((ULONG) 0x00010000)  <br/> |Un fournisseur de banques peut indiquer **fnevIndexing** dans le membre **ulEventType** de la structure **[NOTIFICATION](notification.md)** pour informer l’indexeur qu’un objet est prêt pour l’indexation. Le membre **info** de la structure **NOTIFICATION** contient une structure **[EXTENDED_NOTIFICATION](extended_notification.md)**.  <br/> |
|FS_NONE  <br/> |0x00  <br/> |Un client peut appeler **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** et rechercher le masque de bits renvoyé. **FS_NONE** indique que le dossier ne prend pas en charge le partage.  <br/> |
|FS_SUPPORTS_SHARING  <br/> |0x01  <br/> |Un client peut appeler **IFolderSupport::GetSupportMask** et rechercher le masque de bits renvoyé. **FS_SUPPORTS_SHARING** indique que le dossier prend en charge le partage.  <br/> |
|INDEXING_SEARCH_OWNER  <br/> |((ULONG) 0x00000001)  <br/> |Identifie le processus qui émet une notification à un indexeur indiquant qu’un objet est prêt pour l’indexation.  <br/> |
|MNID_ID  <br/> |Comme définie dans le fichier d’en-tête mapidefs.h du kit de développement logiciel Windows (Kit SDK Windows) de Microsoft  <br/> |Valeur pour le champ **ulKind** de la structure **[MAPINAMEID](mapinameid.md)**.  <br/> |
|MNID_STRING  <br/> |Comme définie dans le fichier d’en-tête mapidefs.h du kit de développement logiciel Windows (Kit SDK Windows) de Microsoft.  <br/> |Valeur pour le champ **ulKind** de la structure **[MAPINAMEID](mapinameid.md)**.  <br/> |
|MSCAP_RES_ANNOTATION  <br/> |((ULONG) 0x00000001)  <br/> |Si un client spécifie **MSCAP_SEL_RESTRICTION** dans *mscapSelector* pour **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** peut renvoyer cette valeur si la banque ignore les paramètres non valides dans une restriction.  <br/> |
|MSCAP_SECURE_FOLDER_HOMEPAGES  <br/> |((ULONG) 0x00000020)  <br/> |Si un client spécifie **MSCAP_SEL_FOLDER** dans *mscapSelector* pour **IMSCapabilities::GetCapabilities**, **GetCapabilities** peut renvoyer cette valeur si la banque est une banque non définie par défaut qui prend en charge les pages d’accueil du dossier.  <br/> |
|STORE_PUSHER_OK  <br/> |((ULONG) 0x00800000)  <br/> |Un client peut accéder à la propriété **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** pour déterminer la caractéristique d’une banque de messages. Si le fournisseur de banques définit l’indicateur **STORE_PUSHER_OK** dans le masque de bits, cela signifie que le gestionnaire de protocole MAPI n’analysera pas la banque et que cette dernière est responsable de la transmission des modifications via l’envoi de notifications à l’indexeur afin d’indexer des messages.  <br/> |
   
### <a name="definitions-for-namespaces"></a>Définitions pour les espaces de noms

Les identificateurs globaux uniques (GUID) suivants représentent les espaces de noms des propriétés nommées. Ils sont indexés par le gestionnaire de protocole MAPI et sont présentés en lecture seule.
  
> [!CAUTION]
> Les propriétés nommées ne doivent pas être utilisées pour créer ou modifier des éléments. 
  
```cpp
const GUID PS_INTERNET_HEADERS  = {0x00020386, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PS_PUBLIC_STRINGS    = {0x00020329, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Address       = {0x00062004, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Appointment   = {0x00062002, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Common        = {0x00062008, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Log           = {0x0006200A, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Meeting       = {0x6ED8DA90, 0x450B, 0x101B, {0x98, 0xDA, 0x00, 0xAA, 0x00, 0x3F, 0x13, 0x05}}; 
const GUID PSETID_Task          = {0x00062003, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
```

#### <a name="mnid_id-properties"></a>Propriétés MNID_ID
  
```cpp
// In PSETID_Address
#define dispidWorkAddressStreet 0x8045
#define dispidWorkAddressCity 0x8046
#define dispidWorkAddressState 0x8047
#define dispidWorkAddressPostalCode 0x8048
#define dispidWorkAddressCountry 0x8049
#define dispidInstMsg 0x8062
#define dispidEmailDisplayName 0x8080
#define dispidEmailOriginalDisplayName 0x8084
```

```cpp
// In PSETID_Appointment
#define dispidLocation 0x8208
#define dispidApptStartWhole 0x820D
#define dispidApptEndWhole 0x820E
#define dispidApptDuration 0x8213
#define dispidRecurring 0x8223
#define dispidAllAttendeesString 0x8238
#define dispidToAttendeesString 0x823B
#define dispidCCAttendeesString 0x823C
```

```cpp
// In PSETID_Common
#define dispidReminderSet 0x8503
#define dispidSmartNoAttach 0x8514
#define dispidCommonStart 0x8516
#define dispidCommonEnd 0x8517
#define dispidRequest 0x8530
#define dispidCompanies 0x8539
#define dispidReminderNextTime 0x8560
```

```cpp
// In PSETID_Log (also known as Journal)
#define dispidLogType 0x8700
#define dispidLogStart 0x8706
#define dispidLogDuration 0x8707
#define dispidLogEnd 0x8708MNID_STRING properties
```

```cpp
// In PSETID_Task
#define dispidTaskStartDate 0x8104
#define dispidTaskDueDate 0x8105
#define dispidTaskActualEffort 0x8110
#define dispidTaskEstimatedEffort 0x8111
#define dispidTaskFRecur 0x8126
```

#### <a name="mnid_string-properties"></a>Propriétés MNID_STRING
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a>Identificateurs d’interface

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

Utilisez la macro `DEFINE_OLEGUID` définie dans le fichier d’en-tête guiddef.h du SDK Windows pour associer le nom symbolique GUID suivant à sa valeur. 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a>Constantes de carnet d’adresses MAPI

Cette section contient les définitions des constantes pour le carnet d’adresses MAPI.
  
### <a name="constants"></a>Constantes

||||
|:-----|:-----|:-----|
|CONTAB_ROOT  <br/> |((ULONG) 0x00000001)  <br/> |Dossier racine d’un objet de carnet d’adresses MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |((ULONG) 0x00000002)  <br/> |Sous-dossier inclus dans le dossier racine de l’objet de carnet d’adresses MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |((ULONG) 0x00000003)  <br/> |Objet de conteneur de carnet d’adresses.  <br/> |
|CONTAB_USER  <br/> |((ULONG) 0x00000004)  <br/> |Objet d’utilisateur de messagerie.  <br/> |
|CONTAB_DISTLIST  <br/> |((ULONG) 0x00000005)  <br/> |Objet de liste de distribution.  <br/> |
   
## <a name="additional-mapi-constants"></a>Constantes MAPI supplémentaires

Cette section contient les définitions des constantes, y compris les codes d’erreur et les identificateurs d’interface utilisés par les API MAPI non exposées et non documentées précédemment.
  
||||
|:-----|:-----|:-----|
|DIALOG_MODAL  <br/> |((ULONG) 0x00000001)  <br/> |Lorsqu’un client appelle la méthode [IAddrBook::Details](iaddrbook-details.md), le client doit définir l’indicateur **DIALOG_MODAL** dans le paramètre _ulFlags_ pour afficher la boîte de dialogue modale montrant les détails sur une entrée particulière de carnet d’adresses. Cette constante est définie dans mapidefs.h.  <br/> |
|ITEMPROC_FORCE  <br/> |0x00000800  <br/> |Dans Outlook 2007, les archives PST encapsulées traitent les règles et le filtrage du courrier indésirable dans les nouveaux messages avant que les clients MAPI soient avertis de nouveaux messages. Un fournisseur ou un client utilisant la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour créer un message dans des archives PST doit définir l’indicateur **ITEMPROC_FORCE** dans le paramètre _ulFlags_ de la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour indiquer à l’archive PST que le message est éligible pour le traitement des règles avant que la banque avertisse les clients à l’écoute de l’arrivée du nouveau message. Notez que ce type de traitement de règles s’applique uniquement aux nouveaux messages créés sur un serveur qui n’est pas un serveur Microsoft Exchange Server, car le serveur Exchange traite les règles pour les messages contenus sur le serveur. Par conséquent, le fournisseur ou le client à l’origine de la création du message doit valider cet indicateur conjointement à **NON_EMS_XP_SAVE**, qui indique que le serveur n’est pas un serveur Exchange.  <br/> |
| MAPI_BG_SESSION  <br/> |0x00200000  <br/> |Un client peut appeler la fonction [MAPILogonEx](mapilogonex.md) en définissant l’indicateur **MAPI_BG_SESSION** dans le paramètre _flFlags_ pour se connecter à une session et effectuer les opérations en arrière-plan. En règle générale, si un client souhaite effectuer un traitement sur un thread d’arrière-plan ou dans un processus distinct d'une façon qui soit compatible avec le thread de premier plan, il doit appeler [MAPILogonEx](mapilogonex.md) avec l’indicateur **MAPI_BG_SESSION**. Ce procédé est par exemple utilisé lorsqu’une application cliente, telle que le moteur d’indexation, ouvre un fichier de dossiers personnels (PST) pour l’accès aux types en arrière-plan.  <br/> |
|MAPI_CACHE_ONLY  <br/> |0x00004000  <br/> |Un client peut appeler la méthode [IAddrBook::OpenEntry](iaddrbook-openentry.md) en définissant l’indicateur **MAPI_CACHE_ONLY** dans le paramètre _ulFlags_ pour ouvrir une entrée de carnet d’adresses et y accéder par la suite exclusivement à partir du cache. Ce procédé est par exemple utilisé dans une application cliente qui souhaite ouvrir la liste d’adresses globale en mode Exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur.  <br/> |
|MAPI_DIALOG_MODELESS  <br/> |0x0000000C  <br/> |Cette valeur peut être transmise à la fonction MAPISendMail Simple MAPI dans le paramètre _ulFlags_ pour spécifier qu’une boîte de dialogue non modale est affichée par l’application de courrier par défaut. Si ni cet indicateur, ni MAPI_DIALOG (0x00000008) ne sont définis, aucune boîte de dialogue ne s’affiche.  <br/> |
|MAPI_NO_CACHE  <br/> |0x00000200  <br/> |Si Microsoft Office Outlook est en mode Exchange mis en cache et qu’une banque a été ouverte en mode mis en cache, le client ou le fournisseur de services peut appeler [IMsgStore::OpenEntry](imsgstore-openentry.md) en définissant l’indicateur **MAPI_NO_CACHE** dans le paramètre _ulFlags_ pour ouvrir un élément ou un dossier dans la banque à distance. Notez que si vous ouvrez la banque de messages avec l’indicateur **MDB_ONLINE** sur le serveur distant, vous n’êtes pas obligé d’utiliser l’indicateur **MAPI_NO_CACHE**.  <br/> |
|MAPI_UNICODE  <br/> |0x80000000  <br/> |Un client ou un fournisseur de services peut appeler la fonction [OpenIMsgOnIStg](openimsgonistg.md) en définissant l’indicateur **MAPI_UNICODE** dans le paramètre _ulFlags_ pour créer des fichiers .msg Unicode. Le fichier [IMessage : IMAPIProp](imessageimapiprop.md) obtenu indique **STORE_UNICODE_OK** dans sa [propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) et prend en charge les propriétés Unicode. Cette constante est définie dans mapidefs.h.  <br/> |
|MDB_ONLINE  <br/> |0x00000100  <br/> |Si Outlook est en mode Exchange mis en cache, le client ou le fournisseur de services peut appeler la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) en définissant l’indicateur **MDB_ONLINE** dans le paramètre _ulFlags_ pour remplacer la connexion à la banque de messages locale et ouvrir la banque sur le serveur distant. Notez que vous ne pouvez pas ouvrir une banque d'informations Exchange en mode mis en cache et en mode non mis en cache simultanément dans la même session MAPI. Si vous avez déjà ouvert la banque de messages mise en cache, vous devez fermer la banque avant de l’ouvrir avec cet indicateur, ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d'informations Exchange sur le serveur distant à l’aide de cet indicateur.  <br/> |
|NON_EMS_XP_SAVE  <br/> |0x00001000  <br/> |Un client peut appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en définissant l’indicateur **NON_EMS_XP_SAVE** dans le paramètre _ulFlags_ pour indiquer que le message n’a pas été remis à partir d’un serveur Exchange. Cet indicateur doit être utilisé conjointement avec l’indicateur **ITEMPROC_FORCE** dans le paramètre _ulFlags_ pour indiquer à l’archive PST que le message est éligible pour le traitement des règles avant que la banque avertisse les clients à l’écoute de l’arrivée du nouveau message. Ce traitement de règle s’applique uniquement aux nouveaux messages créés avec [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) sur un serveur qui n’est pas un serveur Exchange (en pareil cas, le serveur Exchange aurait déjà traité les règles dans le message).  <br/> |
|SPAMFILTER_ONSAVE  <br/> |0x00000080  <br/> |Un client peut appeler [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en définissant l’indicateur **SPAMFILTER_ONSAVE** dans le paramètre _ulFlags_ pour activer le filtrage du courrier indésirable dans un message en cours d’enregistrement. La prise en charge du filtrage du courrier indésirable n’est disponible que si le type d’adresse e-mail de l’expéditeur suit le protocole SMTP et que le message est enregistré dans une banque pour un fichier de dossiers personnels (PST).  <br/> |
|STORE_ITEMPROC  <br/> |0x00200000  <br/> |Si cet indicateur est défini dans la [propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) d’une archive PST encapsulée, il indique que lorsqu’un nouveau message arrive dans la banque, cette dernière traite des règles et effectue le filtrage du courrier indésirable séparément dans le message. La banque appelle ensuite [IMAPISupport::Notify](imapisupport-notify.md), en définissant **fnevNewMail** dans la structure [NOTIFICATION](notification.md) transmise comme paramètre et en envoyant les détails du nouveau message à un client à l’écoute. Par la suite, lorsque le client à l’écoute reçoit la notification, il ne traite pas de règles dans le message.  <br/> |
|STORE_UNICODE_OK  <br/> |0x00040000  <br/> |Si cet indicateur est inclus dans la [propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), il indique que la banque prend en charge le stockage Unicode. Un client peut rechercher la présence de l’indicateur pour décider s’il doit demander des informations Unicode à la banque ou les y enregistrer.  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a>Définitions pour l’archivage d’éléments dans un dossier

Les définitions des constantes suivantes sont des valeurs utilisées pour configurer la [propriété canonique PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a>Définitions pour l’affichage des objets distants

Les définitions des constantes et de macros suivantes s’appliquent à des objets distants. Pour obtenir plus d’informations, consultez la [propriété canonique PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).
  
```cpp
#define DTE_FLAG_REMOTE_VALID0x80000000 
#define DTE_FLAG_ACL_CAPABLE    0x40000000 
#define DTE_MASK_REMOTE        0x0000ff00 
#define DTE_MASK_LOCAL        0x000000ff 
  
#define DTE_IS_REMOTE_VALID(v)(!!((v) & DTE_FLAG_REMOTE_VALID)) 
#define DTE_IS_ACL_CAPABLE(v)(!!((v) & DTE_FLAG_ACL_CAPABLE)) 
#define DTE_REMOTE(v)(((v) & DTE_MASK_REMOTE) >> 8) 
#define DTE_LOCAL(v)((v) & DTE_MASK_LOCAL) 
  
#define DT_ROOM((ULONG) 0x00000007) 
#define DT_EQUIPMENT((ULONG) 0x00000008) 
#define DT_SEC_DISTLIST((ULONG) 0x00000009)
```

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a>Définitions pour le carnet d’adresses Exchange et les codes d’erreur de la banque de messages

Les informations suivantes contiennent des définitions de code d’erreur pour le carnet d’adresses Exchange et la banque de messages, lesquels disposent d’une fonctionnalité de reconnexion. Le dernier appel à un catalogue global déconnecté peut entraîner l’erreur **MAPI_E_END_OF_SESSION**. L’appel doit alors être retenté. 
  
MAPI d’Outlook prend en charge la reconnexion à un serveur de catalogue global sans reconfiguration spéciale, mais certains autres codes d’erreur peuvent être renvoyés au client.
  
||||
|:-----|:-----|:-----|
|MAPI_E_END_OF_SESSION  <br/> |0x80040200  <br/> |Renvoyé si une connexion a été déconnectée.  <br/> |
|MAPI_E_RECONNECTED  <br/> |0x80040125  <br/> |Renvoyé lorsque le jeton de connexion d’appel de procédure distante (RPC) est obsolète. Si le jeton de la transaction actuelle est différent du jeton de la connexion, cela signifie qu’il s’est reconnecté, par conséquent **MAPI_E_RECONNECTED** est renvoyé et peut être traité de la même façon que **MAPI_E_END_OF_SESSION**. L’appel doit être retenté.  <br/> |
|MAPI_E_OFFLINE  <br/> |0x80040126  <br/> |Renvoyé lorsque la connexion est en mode hors ligne. En règle générale, cela signifie que quelque chose s’est produit dans l’environnement, par exemple une défaillance du serveur ou une perte de connectivité réseau. Cette erreur risque surtout de se produire lorsque vous utilisez un profil en mode mis en cache et tentez de contourner le cache pour communiquer avec le serveur. Si le cache n’a jamais réussi à établir en premier lieu une connexion au serveur, il est peut-être dans un état hors connexion où l’erreur **MAPI_E_OFFLINE** peut survenir.  <br/> |
   
Aucune des deux erreurs précédentes n’est renvoyée dans tous les scénarios où elles semblent s’appliquer. Dans la plupart des cas, **MAPI\_E_NETWORK_ERROR** ou **MAPI_E_CALL_FAILED** sera renvoyée. Aucune ne s’affiche si le téléchargement [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440) est utilisé. 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a>Définitions des quotas de mode mis en cache de la boîte aux lettres du serveur Exchange

Les définitions des constantes suivantes sont utilisées par Microsoft Outlook 2010 et Microsoft Outlook 2013 pour définir des quotas de profil du mode mis en cache Exchange équivalents aux quotas de boîte aux lettres Exchange à défaut de n’être disponibles qu’avec un profil en ligne.
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

Ces propriétés sont associées à leurs propriétés en ligne correspondantes et contiennent les mêmes valeurs en kilo-octets. PR_QUOTA_WARNING est associé à PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND à PR_QUOTA_PROHIBIT_SEND_QUOTA et PR_QUOTA_RECEIVE à PR_PROHIBIT_RECEIVE_QUOTA.
  
### <a name="definitions-for-message-format"></a>Définitions du format des messages

Les définitions des constantes suivantes sont des valeurs utilisées pour configurer la [propriété canonique PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a>Définitions pour utiliser RPC sur HTTP

Consultez la rubrique [Propriété canonique PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) pour obtenir les définitions des constantes utilisées comme des indicateurs pour définir la propriété. 
  
Consultez la rubrique [Propriété canonique PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) pour obtenir les définitions des constantes utilisées pour définir la propriété. 
  
### <a name="identifiers"></a>Identificateurs

Utilisez la macro `DEFINE_OLEGUID` définie dans le fichier d’en-tête guiddef.h du kit de développement logiciel Windows (Kit SDK Windows) de Microsoft pour associer les noms symboliques (GUID) suivants à leurs valeurs. 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

L’identificateur suivant concerne la section du profil Capone d’un carnet d’adresses qui, dans le cadre de la prise en charge de plusieurs boîtes aux lettres Exchange ([MultiEx](using-multiple-exchange-accounts.md)), contient la propriété [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) permettant de désactiver efficacement le conteneur par défaut spécifié par [SetDefaultDir](iaddrbook-setdefaultdir.md).
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a>Identificateurs d’interface

#### <a name="imapisync"></a>IMAPISync
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a>IMAPISyncProgressCallback
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iid_icontabadmin"></a>IID_IContabAdmin
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iid_imapisecuremessage"></a>IID_IMAPISECUREMESSAGE
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iid_imapigetsession"></a>IID_IMAPIGetSession
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a>Identificateurs d’interface de remplacement du gestionnaire PST

#### <a name="iid_ipstoverridereq"></a>IID_IPSTOVERRIDEREQ
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iid_ipstoverride1"></a>IID_IPSTOVERRIDE1
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a>Voir aussi

- [À propos des ajouts MAPI](about-mapi-additions.md) 
- [À propos des propriétés nommées utilisées par Outlook](about-named-properties-used-by-outlook.md)
- [Accès à une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Ouvrir une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Gérer un message dans un fichier OST sans appeler de synchronisation en mode Exchange mis en cache](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

