---
title: Constantes MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4f84ed318fa53877acd9d4759b81c140d2b32e6b
ms.sourcegitcommit: 6a8c758e690c4b7f3ab6d40635606efd31a3cc07
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/03/2018
ms.locfileid: "25361484"
---
# <a name="mapi-constants"></a><span data-ttu-id="fcde3-103">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="fcde3-103">MAPI constants</span></span>

<span data-ttu-id="fcde3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcde3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcde3-105">Cette rubrique contient des définitions de constantes, les déclarations d’interface MAPI et les identificateurs de classe et d’interface utilisés par les API de MAPI.</span><span class="sxs-lookup"><span data-stu-id="fcde3-105">This topic contains constant definitions, MAPI interface declarations, and class and interface identifiers used by the MAPI APIs.</span></span>
  
## <a name="class-and-interface-identifiers"></a><span data-ttu-id="fcde3-106">Identificateurs de classe et d’interface</span><span class="sxs-lookup"><span data-stu-id="fcde3-106">Class and interface identifiers</span></span>

<span data-ttu-id="fcde3-107">Utilisez la macro DEFINE_GUID définie dans le guiddef.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows pour associer les noms symboliques identificateur global unique (GUID) à leurs valeurs, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="fcde3-107">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values, unless otherwise indicated.</span></span>
  
## <a name="attachment-security-conversion-api"></a><span data-ttu-id="fcde3-108">Conversion de sécurité des pièces jointes API</span><span class="sxs-lookup"><span data-stu-id="fcde3-108">Attachment security conversion API</span></span>

<span data-ttu-id="fcde3-109">Cette section contient des définitions de constantes et les identificateurs d’interface de l’API de sécurité des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="fcde3-109">This section contains constant definitions and interface identifiers for the Attachment Security API.</span></span>
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

<span data-ttu-id="fcde3-110">Utilisez la macro MAPIMETHOD définie dans le mapidefs.h de fichier d’en-tête SDK Windows pour définir la fonction virtuelle pure **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span><span class="sxs-lookup"><span data-stu-id="fcde3-110">Use the MAPIMETHOD macro defined in the Windows SDK header file mapidefs.h to define the pure virtual function **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span></span> 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

<span data-ttu-id="fcde3-111">Utilisez la macro DECLARE_MAPI_INTERFACE_ définie dans le mapidefs.h de fichier d’en-tête SDK Windows pour définir la table de méthodes virtuelles pour **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="fcde3-111">Use the DECLARE_MAPI_INTERFACE_ macro defined in the Windows SDK header file mapidefs.h to define the virtual method table for **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span></span> 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a><span data-ttu-id="fcde3-112">Conversion MAPI MIME API</span><span class="sxs-lookup"><span data-stu-id="fcde3-112">MAPI-MIME conversion API</span></span>

<span data-ttu-id="fcde3-113">Cette section contient des définitions de constantes et les identificateurs de classe et l’interface de l’API de Conversion MAPI MIME.</span><span class="sxs-lookup"><span data-stu-id="fcde3-113">This section contains constant definitions and class and interface identifiers for the MAPI-MIME Conversion API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="fcde3-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="fcde3-114">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcde3-115">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="fcde3-115">CCSF_SMTP</span></span>  <br/> |<span data-ttu-id="fcde3-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="fcde3-116">0x0002</span></span>  <br/> |
|<span data-ttu-id="fcde3-117">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="fcde3-117">CCSF_NOHEADERS</span></span>  <br/> |<span data-ttu-id="fcde3-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="fcde3-118">0x0004</span></span>  <br/> |
|<span data-ttu-id="fcde3-119">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="fcde3-119">CCSF_USE_TNEF</span></span>  <br/> | <span data-ttu-id="fcde3-120">0x0010</span><span class="sxs-lookup"><span data-stu-id="fcde3-120">0x0010</span></span>  <br/> |
|<span data-ttu-id="fcde3-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="fcde3-121">CCSF_INCLUDE_BCC</span></span>  <br/> |<span data-ttu-id="fcde3-122">0 x 0020</span><span class="sxs-lookup"><span data-stu-id="fcde3-122">0x0020</span></span>  <br/> |
|<span data-ttu-id="fcde3-123">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="fcde3-123">CCSF_8BITHEADERS</span></span>  <br/> | <span data-ttu-id="fcde3-124">0x0040</span><span class="sxs-lookup"><span data-stu-id="fcde3-124">0x0040</span></span>  <br/> |
|<span data-ttu-id="fcde3-125">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="fcde3-125">CCSF_USE_RTF</span></span>  <br/> |<span data-ttu-id="fcde3-126">0 x 0080</span><span class="sxs-lookup"><span data-stu-id="fcde3-126">0x0080</span></span>  <br/> |
|<span data-ttu-id="fcde3-127">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="fcde3-127">CCSF_PLAIN_TEXT_ONLY</span></span>  <br/> |<span data-ttu-id="fcde3-128">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="fcde3-128">0x1000</span></span>  <br/> |
|<span data-ttu-id="fcde3-129">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="fcde3-129">CCSF_NO_MSGID</span></span>  <br/> |<span data-ttu-id="fcde3-130">0 x 4000</span><span class="sxs-lookup"><span data-stu-id="fcde3-130">0x4000</span></span>  <br/> |
|<span data-ttu-id="fcde3-131">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="fcde3-131">CCSF_GLOBAL_MESSAGE</span></span>  <br/> |<span data-ttu-id="fcde3-132">0 x 00200000</span><span class="sxs-lookup"><span data-stu-id="fcde3-132">0x00200000</span></span>  <br/> |
|<span data-ttu-id="fcde3-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="fcde3-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="fcde3-134">*Comme défini dans le fichier d’en-tête winerror.h Kit de développement logiciel (SDK) de Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="fcde3-134">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="fcde3-135">Identificateurs de classe</span><span class="sxs-lookup"><span data-stu-id="fcde3-135">Class identifiers</span></span>

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a><span data-ttu-id="fcde3-136">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="fcde3-136">Interface identifiers</span></span>

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a><span data-ttu-id="fcde3-137">État en mode hors connexion API</span><span class="sxs-lookup"><span data-stu-id="fcde3-137">Offline State API</span></span>

<span data-ttu-id="fcde3-138">Cette section contient des définitions de constantes et les identificateurs de classe et l’interface de l’API de l’état en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="fcde3-138">This section contains constant definitions and class and interface identifiers for the Offline State API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="fcde3-139">Constantes</span><span class="sxs-lookup"><span data-stu-id="fcde3-139">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcde3-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="fcde3-140">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="fcde3-141">*Comme défini dans le fichier d’en-tête winerror.h Kit de développement logiciel (SDK) de Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="fcde3-141">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="fcde3-142">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="fcde3-142">E_NOINTERFACE</span></span>  <br/> | <span data-ttu-id="fcde3-143">*Comme défini dans le fichier d’en-tête winerror.h (SDK) Windows*</span><span class="sxs-lookup"><span data-stu-id="fcde3-143">*As defined in the Windows (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="fcde3-144">MAPIOFFLINE_ADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="fcde3-144">MAPIOFFLINE_ADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="fcde3-145">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="fcde3-145">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="fcde3-146">MAPIOFFLINE_UNADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="fcde3-146">MAPIOFFLINE_UNADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="fcde3-147">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="fcde3-147">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="fcde3-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="fcde3-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span></span>  <br/> |<span data-ttu-id="fcde3-149">1</span><span class="sxs-lookup"><span data-stu-id="fcde3-149">1</span></span>  <br/> |
|<span data-ttu-id="fcde3-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="fcde3-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="fcde3-151">0 x 1</span><span class="sxs-lookup"><span data-stu-id="fcde3-151">0x1</span></span>  <br/> |
|<span data-ttu-id="fcde3-152">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="fcde3-152">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="fcde3-153">0 x 2</span><span class="sxs-lookup"><span data-stu-id="fcde3-153">0x2</span></span>  <br/> |
|<span data-ttu-id="fcde3-154">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="fcde3-154">MAPIOFFLINE_FLAG_BLOCK</span></span>  <br/> |<span data-ttu-id="fcde3-155">0 x 00002000</span><span class="sxs-lookup"><span data-stu-id="fcde3-155">0x00002000</span></span>  <br/> |
|<span data-ttu-id="fcde3-156">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="fcde3-156">MAPIOFFLINE_FLAG_DEFAULT</span></span>  <br/> |<span data-ttu-id="fcde3-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcde3-157">0x00000000</span></span>  <br/> |
|<span data-ttu-id="fcde3-158">MAPIOFFLINE_STATE_ALL</span><span class="sxs-lookup"><span data-stu-id="fcde3-158">MAPIOFFLINE_STATE_ALL</span></span>  <br/> |<span data-ttu-id="fcde3-159">0x003f037f</span><span class="sxs-lookup"><span data-stu-id="fcde3-159">0x003f037f</span></span>  <br/> |
|<span data-ttu-id="fcde3-160">**En ligne ou hors connexion**</span><span class="sxs-lookup"><span data-stu-id="fcde3-160">**Online or offline**</span></span> <br/> ||
|<span data-ttu-id="fcde3-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span><span class="sxs-lookup"><span data-stu-id="fcde3-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span></span>  <br/> |<span data-ttu-id="fcde3-162">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="fcde3-162">0x00000003</span></span>  <br/> |
|<span data-ttu-id="fcde3-163">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="fcde3-163">MAPIOFFLINE_STATE_OFFLINE</span></span>  <br/> |<span data-ttu-id="fcde3-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fcde3-164">0x00000001</span></span>  <br/> |
|<span data-ttu-id="fcde3-165">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="fcde3-165">MAPIOFFLINE_STATE_ONLINE</span></span>  <br/> |<span data-ttu-id="fcde3-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fcde3-166">0x00000002</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="fcde3-167">Identificateurs de classe</span><span class="sxs-lookup"><span data-stu-id="fcde3-167">Class identifiers</span></span>

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a><span data-ttu-id="fcde3-168">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="fcde3-168">Interface identifiers</span></span>

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

## <a name="outlook-named-properties"></a><span data-ttu-id="fcde3-169">Outlook des propriétés nommée</span><span class="sxs-lookup"><span data-stu-id="fcde3-169">Outlook named properties</span></span>

<span data-ttu-id="fcde3-170">Cette section contient des définitions de constantes pour les propriétés nommées et leurs espaces de noms et des constantes connexes.</span><span class="sxs-lookup"><span data-stu-id="fcde3-170">This section contains constant definitions for named properties and their namespaces, and other related constants.</span></span>
  
### <a name="definitions-for-named-properties"></a><span data-ttu-id="fcde3-171">Définitions de propriétés nommées</span><span class="sxs-lookup"><span data-stu-id="fcde3-171">Definitions for named properties</span></span>

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

### <a name="definitions-for-namespaces"></a><span data-ttu-id="fcde3-172">Définitions pour les espaces de noms</span><span class="sxs-lookup"><span data-stu-id="fcde3-172">Definitions for namespaces</span></span>

<span data-ttu-id="fcde3-173">Les identificateurs globaux uniques (GUID) suivantes représentent les espaces de noms des propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="fcde3-173">The following globally unique identifiers (GUIDs) represent the namespaces of the named properties.</span></span>
  
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

<span data-ttu-id="fcde3-174">Reportez-vous à la section emplacement de stockage MAPI pour les définitions PSETID.</span><span class="sxs-lookup"><span data-stu-id="fcde3-174">Refer to the section MAPI Store for the PSETID definitions.</span></span>
  
### <a name="other-constants"></a><span data-ttu-id="fcde3-175">Autres constantes</span><span class="sxs-lookup"><span data-stu-id="fcde3-175">Other constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcde3-176">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="fcde3-176">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="fcde3-177">0xD000000</span><span class="sxs-lookup"><span data-stu-id="fcde3-177">0xD000000</span></span>  <br/> |
|<span data-ttu-id="fcde3-178">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="fcde3-178">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="fcde3-179">0x2000000</span><span class="sxs-lookup"><span data-stu-id="fcde3-179">0x2000000</span></span>  <br/> |
|<span data-ttu-id="fcde3-180">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="fcde3-180">MNID_ID</span></span>  <br/> | <span data-ttu-id="fcde3-181">*Comme défini dans le mapidefs.h de fichier d’en-tête.*</span><span class="sxs-lookup"><span data-stu-id="fcde3-181">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="fcde3-182">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="fcde3-182">MNID_STRING</span></span>  <br/> | <span data-ttu-id="fcde3-183">*Comme défini dans le mapidefs.h de fichier d’en-tête.*</span><span class="sxs-lookup"><span data-stu-id="fcde3-183">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="fcde3-184">mtgNone</span><span class="sxs-lookup"><span data-stu-id="fcde3-184">mtgNone</span></span>  <br/> |<span data-ttu-id="fcde3-185">0 x 0</span><span class="sxs-lookup"><span data-stu-id="fcde3-185">0x0</span></span>  <br/> |
|<span data-ttu-id="fcde3-186">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="fcde3-186">mtgRequest</span></span>  <br/> |<span data-ttu-id="fcde3-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fcde3-187">0x00000001</span></span>  <br/> |
|<span data-ttu-id="fcde3-188">mtgFullUpdate</span><span class="sxs-lookup"><span data-stu-id="fcde3-188">mtgFullUpdate</span></span>  <br/> |<span data-ttu-id="fcde3-189">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-189">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-190">mtgInfoUpdate</span><span class="sxs-lookup"><span data-stu-id="fcde3-190">mtgInfoUpdate</span></span>  <br/> |<span data-ttu-id="fcde3-191">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="fcde3-191">0x00020000</span></span>  <br/> |
|<span data-ttu-id="fcde3-192">mtgOutofDate</span><span class="sxs-lookup"><span data-stu-id="fcde3-192">mtgOutofDate</span></span>  <br/> |<span data-ttu-id="fcde3-193">0 x 00080000</span><span class="sxs-lookup"><span data-stu-id="fcde3-193">0x00080000</span></span>  <br/> |
|<span data-ttu-id="fcde3-194">mtgDelegated</span><span class="sxs-lookup"><span data-stu-id="fcde3-194">mtgDelegated</span></span>  <br/> |<span data-ttu-id="fcde3-195">0 x 00100000</span><span class="sxs-lookup"><span data-stu-id="fcde3-195">0x00100000</span></span>  <br/> |
   
## <a name="replication-api"></a><span data-ttu-id="fcde3-196">API de réplication</span><span class="sxs-lookup"><span data-stu-id="fcde3-196">Replication API</span></span>

<span data-ttu-id="fcde3-197">Cette section contient des définitions de constantes, les déclarations d’interface MAPI et identificateurs de classe et d’interface pour l’API de réplication.</span><span class="sxs-lookup"><span data-stu-id="fcde3-197">This section contains constant definitions, MAPI interface declarations, and class and interface identifiers for the Replication API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="fcde3-198">Constantes</span><span class="sxs-lookup"><span data-stu-id="fcde3-198">Constants</span></span>

<span data-ttu-id="fcde3-199">Vous trouverez ci-dessous une structure [MAPIUID](mapiuid.md) qui identifie un fournisseur de services MAPI :</span><span class="sxs-lookup"><span data-stu-id="fcde3-199">The following is a [MAPIUID](mapiuid.md) structure identifying a MAPI service provider:</span></span> 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|<span data-ttu-id="fcde3-200">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-200">DNH_OK</span></span>  <br/> |<span data-ttu-id="fcde3-201">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-201">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-202">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-202">DNT_OK</span></span>  <br/> |<span data-ttu-id="fcde3-203">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-203">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-204">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="fcde3-204">HSF_LOCAL</span></span>  <br/> |<span data-ttu-id="fcde3-205">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="fcde3-205">0x00000008</span></span>  <br/> |
|<span data-ttu-id="fcde3-206">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="fcde3-206">HSF_COPYDESTRUCTIVE</span></span>  <br/> |<span data-ttu-id="fcde3-207">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="fcde3-207">0x00000010</span></span>  <br/> |
|<span data-ttu-id="fcde3-208">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-208">HSF_OK</span></span>  <br/> |<span data-ttu-id="fcde3-209">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-209">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-210">MDB_OST_LOGON_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fcde3-210">MDB_OST_LOGON_UNICODE</span></span>  <br/> |<span data-ttu-id="fcde3-211">((ULONG) 0X00000800)</span><span class="sxs-lookup"><span data-stu-id="fcde3-211">((ULONG) 0x00000800)</span></span>  <br/> |
|<span data-ttu-id="fcde3-212">MDB_OST_LOGON_ANSI</span><span class="sxs-lookup"><span data-stu-id="fcde3-212">MDB_OST_LOGON_ANSI</span></span>  <br/> |<span data-ttu-id="fcde3-213">((ULONG) 0 X 00001000)</span><span class="sxs-lookup"><span data-stu-id="fcde3-213">((ULONG) 0x00001000)</span></span>  <br/> |
|<span data-ttu-id="fcde3-214">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="fcde3-214">SHOW_SOFT_DELETES</span></span>  <br/> |<span data-ttu-id="fcde3-215">((ULONG) 0 X 00000002)</span><span class="sxs-lookup"><span data-stu-id="fcde3-215">((ULONG) 0x00000002)</span></span>  <br/> |
|<span data-ttu-id="fcde3-216">SS_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="fcde3-216">SS_ACTIVE</span></span>  <br/> |<span data-ttu-id="fcde3-217">0</span><span class="sxs-lookup"><span data-stu-id="fcde3-217">0</span></span>  <br/> |
|<span data-ttu-id="fcde3-218">SS_SUSPENDED</span><span class="sxs-lookup"><span data-stu-id="fcde3-218">SS_SUSPENDED</span></span>  <br/> |<span data-ttu-id="fcde3-219">1</span><span class="sxs-lookup"><span data-stu-id="fcde3-219">1</span></span>  <br/> |
|<span data-ttu-id="fcde3-220">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="fcde3-220">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="fcde3-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fcde3-221">0x00000001</span></span>  <br/> |
|<span data-ttu-id="fcde3-222">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="fcde3-222">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="fcde3-223">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fcde3-223">0x00000002</span></span>  <br/> |
|<span data-ttu-id="fcde3-224">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="fcde3-224">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="fcde3-225">0 x 00000040</span><span class="sxs-lookup"><span data-stu-id="fcde3-225">0x00000040</span></span>  <br/> |
|<span data-ttu-id="fcde3-226">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="fcde3-226">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="fcde3-227">0x00000080</span><span class="sxs-lookup"><span data-stu-id="fcde3-227">0x00000080</span></span>  <br/> |
|<span data-ttu-id="fcde3-228">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="fcde3-228">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="fcde3-229">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="fcde3-229">0x00000200</span></span>  <br/> |
|<span data-ttu-id="fcde3-230">SYNC_BACKGROUND</span><span class="sxs-lookup"><span data-stu-id="fcde3-230">SYNC_BACKGROUND</span></span>  <br/> |<span data-ttu-id="fcde3-231">0 x 00001000</span><span class="sxs-lookup"><span data-stu-id="fcde3-231">0x00001000</span></span>  <br/> |
|<span data-ttu-id="fcde3-232">SYNC_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="fcde3-232">SYNC_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="fcde3-233">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="fcde3-233">0x00020000</span></span>  <br/> |
|<span data-ttu-id="fcde3-234">SYNC_HEADERS</span><span class="sxs-lookup"><span data-stu-id="fcde3-234">SYNC_HEADERS</span></span>  <br/> |<span data-ttu-id="fcde3-235">0x02000000</span><span class="sxs-lookup"><span data-stu-id="fcde3-235">0x02000000</span></span>  <br/> |
|<span data-ttu-id="fcde3-236">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-236">UPC_OK</span></span>  <br/> |<span data-ttu-id="fcde3-237">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-237">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-238">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="fcde3-238">UPD_ASSOC</span></span>  <br/> |<span data-ttu-id="fcde3-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fcde3-239">0x00000001</span></span>  <br/> |
|<span data-ttu-id="fcde3-240">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="fcde3-240">UPD_MOV</span></span>  <br/> |<span data-ttu-id="fcde3-241">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fcde3-241">0x00000002</span></span>  <br/> |
|<span data-ttu-id="fcde3-242">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-242">UPD_OK</span></span>  <br/> |<span data-ttu-id="fcde3-243">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-243">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-244">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="fcde3-244">UPD_MOVED</span></span>  <br/> |<span data-ttu-id="fcde3-245">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="fcde3-245">0x00020000</span></span>  <br/> |
|<span data-ttu-id="fcde3-246">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="fcde3-246">UPD_UPDATE</span></span>  <br/> |<span data-ttu-id="fcde3-247">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="fcde3-247">0x00040000</span></span>  <br/> |
|<span data-ttu-id="fcde3-248">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="fcde3-248">UPD_COMMIT</span></span>  <br/> |<span data-ttu-id="fcde3-249">0 x 00080000</span><span class="sxs-lookup"><span data-stu-id="fcde3-249">0x00080000</span></span>  <br/> |
|<span data-ttu-id="fcde3-250">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="fcde3-250">UPF_NEW</span></span>  <br/> |<span data-ttu-id="fcde3-251">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fcde3-251">0x00000001</span></span>  <br/> |
|<span data-ttu-id="fcde3-252">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="fcde3-252">UPF_MOD_PARENT</span></span>  <br/> |<span data-ttu-id="fcde3-253">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fcde3-253">0x00000002</span></span>  <br/> |
|<span data-ttu-id="fcde3-254">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="fcde3-254">UPF_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="fcde3-255">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="fcde3-255">0x00000004</span></span>  <br/> |
|<span data-ttu-id="fcde3-256">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="fcde3-256">UPF_DEL</span></span>  <br/> |<span data-ttu-id="fcde3-257">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="fcde3-257">0x00000008</span></span>  <br/> |
|<span data-ttu-id="fcde3-258">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-258">UPF_OK</span></span>  <br/> |<span data-ttu-id="fcde3-259">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-259">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-260">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-260">UPH_OK</span></span>  <br/> |<span data-ttu-id="fcde3-261">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-261">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-262">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="fcde3-262">UPM_ASSOC</span></span>  <br/> |<span data-ttu-id="fcde3-263">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fcde3-263">0x00000001</span></span>  <br/> |
|<span data-ttu-id="fcde3-264">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="fcde3-264">UPM_NEW</span></span>  <br/> |<span data-ttu-id="fcde3-265">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fcde3-265">0x00000002</span></span>  <br/> |
|<span data-ttu-id="fcde3-266">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="fcde3-266">UPM_MOV</span></span>  <br/> |<span data-ttu-id="fcde3-267">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="fcde3-267">0x00000004</span></span>  <br/> |
|<span data-ttu-id="fcde3-268">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="fcde3-268">UPM_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="fcde3-269">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="fcde3-269">0x00000008</span></span>  <br/> |
|<span data-ttu-id="fcde3-270">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="fcde3-270">UPM_HEADER</span></span>  <br/> |<span data-ttu-id="fcde3-271">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="fcde3-271">0x00000010</span></span>  <br/> |
|<span data-ttu-id="fcde3-272">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-272">UPM_OK</span></span>  <br/> |<span data-ttu-id="fcde3-273">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-273">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-274">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="fcde3-274">UPM_MOVED</span></span>  <br/> |<span data-ttu-id="fcde3-275">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="fcde3-275">0x00020000</span></span>  <br/> |
|<span data-ttu-id="fcde3-276">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="fcde3-276">UPM_COMMIT</span></span>  <br/> |<span data-ttu-id="fcde3-277">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="fcde3-277">0x00040000</span></span>  <br/> |
|<span data-ttu-id="fcde3-278">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="fcde3-278">UPM_DELETE</span></span>  <br/> |<span data-ttu-id="fcde3-279">0 x 00080000</span><span class="sxs-lookup"><span data-stu-id="fcde3-279">0x00080000</span></span>  <br/> |
|<span data-ttu-id="fcde3-280">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="fcde3-280">UPM_SAVE</span></span>  <br/> |<span data-ttu-id="fcde3-281">0 x 00100000</span><span class="sxs-lookup"><span data-stu-id="fcde3-281">0x00100000</span></span>  <br/> |
|<span data-ttu-id="fcde3-282">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="fcde3-282">UPR_ASSOC</span></span>  <br/> |<span data-ttu-id="fcde3-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fcde3-283">0x00000001</span></span>  <br/> |
|<span data-ttu-id="fcde3-284">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="fcde3-284">UPR_READ</span></span>  <br/> |<span data-ttu-id="fcde3-285">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fcde3-285">0x00000002</span></span>  <br/> |
|<span data-ttu-id="fcde3-286">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-286">UPR_OK</span></span>  <br/> |<span data-ttu-id="fcde3-287">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-287">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-288">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="fcde3-288">UPR_COMMIT</span></span>  <br/> |<span data-ttu-id="fcde3-289">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="fcde3-289">0x00020000</span></span>  <br/> |
|<span data-ttu-id="fcde3-290">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="fcde3-290">UPS_UPLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="fcde3-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fcde3-291">0x00000001</span></span>  <br/> |
|<span data-ttu-id="fcde3-292">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="fcde3-292">UPS_DNLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="fcde3-293">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fcde3-293">0x00000002</span></span>  <br/> |
|<span data-ttu-id="fcde3-294">UPS_ONE_FOLDER</span><span class="sxs-lookup"><span data-stu-id="fcde3-294">UPS_ONE_FOLDER</span></span>  <br/> |<span data-ttu-id="fcde3-295">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="fcde3-295">0x00000004</span></span>  <br/> |
|<span data-ttu-id="fcde3-296">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="fcde3-296">UPS_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="fcde3-297">0x00000080</span><span class="sxs-lookup"><span data-stu-id="fcde3-297">0x00000080</span></span>  <br/> |
|<span data-ttu-id="fcde3-298">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-298">UPS_OK</span></span>  <br/> |<span data-ttu-id="fcde3-299">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-299">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-300">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-300">UPT_OK</span></span>  <br/> |<span data-ttu-id="fcde3-301">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-301">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-302">UPT_PUBLIC</span><span class="sxs-lookup"><span data-stu-id="fcde3-302">UPT_PUBLIC</span></span>  <br/> |<span data-ttu-id="fcde3-303">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fcde3-303">0x00000001</span></span>  <br/> |
|<span data-ttu-id="fcde3-304">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="fcde3-304">UPV_ERROR</span></span>  <br/> |<span data-ttu-id="fcde3-305">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="fcde3-305">0x00010000</span></span>  <br/> |
|<span data-ttu-id="fcde3-306">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="fcde3-306">UPV_DIRTY</span></span>  <br/> |<span data-ttu-id="fcde3-307">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="fcde3-307">0x00020000</span></span>  <br/> |
|<span data-ttu-id="fcde3-308">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="fcde3-308">UPV_COMMIT</span></span>  <br/> |<span data-ttu-id="fcde3-309">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="fcde3-309">0x00040000</span></span>  <br/> |
   
### <a name="interface-declarations"></a><span data-ttu-id="fcde3-310">Déclarations d’interface</span><span class="sxs-lookup"><span data-stu-id="fcde3-310">Interface declarations</span></span>

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a><span data-ttu-id="fcde3-311">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="fcde3-311">Interface identifiers</span></span>

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

<span data-ttu-id="fcde3-312">Utilisez les deux identificateurs d’interface suivant avec [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md)ou [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir et ignorer tout fournisseur de contrôle sur un objet folder et un objet de message, respectivement.</span><span class="sxs-lookup"><span data-stu-id="fcde3-312">Use the two following interface identifiers with [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), or [IMsgStore::OpenEntry](imsgstore-openentry.md) to open and ignore any provider check on a folder object and a message object, respectively.</span></span> 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a><span data-ttu-id="fcde3-313">Emplacement de stockage MAPI</span><span class="sxs-lookup"><span data-stu-id="fcde3-313">MAPI store</span></span>

<span data-ttu-id="fcde3-314">Cette section contient des définitions de constantes et identificateurs d’interface utilisé par les API de cette interface avec un magasin MAPI.</span><span class="sxs-lookup"><span data-stu-id="fcde3-314">This section contains constant definitions and interface identifiers used by APIs that interface with a MAPI store.</span></span>
  
### <a name="constants"></a><span data-ttu-id="fcde3-315">Constantes</span><span class="sxs-lookup"><span data-stu-id="fcde3-315">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="fcde3-316">fnevIndexing</span><span class="sxs-lookup"><span data-stu-id="fcde3-316">fnevIndexing</span></span>  <br/> |<span data-ttu-id="fcde3-317">((ULONG) 0 X 00010000)</span><span class="sxs-lookup"><span data-stu-id="fcde3-317">((ULONG) 0x00010000)</span></span>  <br/> |<span data-ttu-id="fcde3-318">Un fournisseur de magasins peut spécifier **fnevIndexing** dans le membre **ulEventType** de la structure de **[NOTIFICATION](notification.md)** pour signaler l’indexeur qu’un objet est prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="fcde3-318">A store provider can specify **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure to notify the indexer that an object is ready for indexing.</span></span> <span data-ttu-id="fcde3-319">Membre de la structure de **NOTIFICATION** **info** contient une structure **[EXTENDED_NOTIFICATION](extended_notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="fcde3-319">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="fcde3-320">FS_NONE</span><span class="sxs-lookup"><span data-stu-id="fcde3-320">FS_NONE</span></span>  <br/> |<span data-ttu-id="fcde3-321">0 x 00</span><span class="sxs-lookup"><span data-stu-id="fcde3-321">0x00</span></span>  <br/> |<span data-ttu-id="fcde3-322">Un client peut appeler **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** et vérification pour le masque de bits retournée.</span><span class="sxs-lookup"><span data-stu-id="fcde3-322">A client can call **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** and check for the returned bitmask.</span></span> <span data-ttu-id="fcde3-323">**FS_NONE** indique que le dossier ne prend pas en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="fcde3-323">**FS_NONE** indicates that the folder does not support sharing.</span></span>  <br/> |
|<span data-ttu-id="fcde3-324">FS_SUPPORTS_SHARING</span><span class="sxs-lookup"><span data-stu-id="fcde3-324">FS_SUPPORTS_SHARING</span></span>  <br/> |<span data-ttu-id="fcde3-325">0x01</span><span class="sxs-lookup"><span data-stu-id="fcde3-325">0x01</span></span>  <br/> |<span data-ttu-id="fcde3-326">Un client peut appeler **IFolderSupport::GetSupportMask** et vérification pour le masque de bits retournée.</span><span class="sxs-lookup"><span data-stu-id="fcde3-326">A client can call **IFolderSupport::GetSupportMask** and check for the returned bitmask.</span></span> <span data-ttu-id="fcde3-327">**FS_SUPPORTS_SHARING** indique que le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="fcde3-327">**FS_SUPPORTS_SHARING** indicates that the folder supports sharing.</span></span>  <br/> |
|<span data-ttu-id="fcde3-328">INDEXING_SEARCH_OWNER</span><span class="sxs-lookup"><span data-stu-id="fcde3-328">INDEXING_SEARCH_OWNER</span></span>  <br/> |<span data-ttu-id="fcde3-329">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="fcde3-329">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="fcde3-330">Identifie le processus qui est envoi une notification à un indexeur qu’un objet est prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="fcde3-330">Identifies the process that is pushing a notification to an indexer that an object is ready for indexing.</span></span>  <br/> |
|<span data-ttu-id="fcde3-331">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="fcde3-331">MNID_ID</span></span>  <br/> |<span data-ttu-id="fcde3-332">Comme défini dans le mapidefs.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="fcde3-332">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h</span></span>  <br/> |<span data-ttu-id="fcde3-333">Une valeur pour le champ **ulKind** de la structure **[MAPINAMEID](mapinameid.md)** .</span><span class="sxs-lookup"><span data-stu-id="fcde3-333">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="fcde3-334">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="fcde3-334">MNID_STRING</span></span>  <br/> |<span data-ttu-id="fcde3-335">Comme défini dans le mapidefs.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fcde3-335">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h.</span></span>  <br/> |<span data-ttu-id="fcde3-336">Une valeur pour le champ **ulKind** de la structure **[MAPINAMEID](mapinameid.md)** .</span><span class="sxs-lookup"><span data-stu-id="fcde3-336">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="fcde3-337">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="fcde3-337">MSCAP_RES_ANNOTATION</span></span>  <br/> |<span data-ttu-id="fcde3-338">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="fcde3-338">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="fcde3-339">Si un client spécifie **MSCAP_SEL_RESTRICTION** en *mscapSelector* de **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** peut renvoyer cette valeur si la banque ignore les paramètres non valides dans une restriction.</span><span class="sxs-lookup"><span data-stu-id="fcde3-339">If a client specifies **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  for **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** can return this value if the store ignores invalid parameters in a restriction.</span></span>  <br/> |
|<span data-ttu-id="fcde3-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="fcde3-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>  <br/> |<span data-ttu-id="fcde3-341">((ULONG) 0 X 00000020)</span><span class="sxs-lookup"><span data-stu-id="fcde3-341">((ULONG) 0x00000020)</span></span>  <br/> |<span data-ttu-id="fcde3-342">Si un client spécifie **MSCAP_SEL_FOLDER** en *mscapSelector* de **IMSCapabilities::GetCapabilities**, **GetCapabilities** peut renvoyer cette valeur si le magasin est un magasin par défaut qui prend en charge les pages d’accueil du dossier.</span><span class="sxs-lookup"><span data-stu-id="fcde3-342">If a client specifies **MSCAP_SEL_FOLDER** in  *mscapSelector*  for **IMSCapabilities::GetCapabilities**, **GetCapabilities** can return this value if the store is a non-default store that supports folder home pages.</span></span>  <br/> |
|<span data-ttu-id="fcde3-343">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-343">STORE_PUSHER_OK</span></span>  <br/> |<span data-ttu-id="fcde3-344">((ULONG) 0 X 00800000)</span><span class="sxs-lookup"><span data-stu-id="fcde3-344">((ULONG) 0x00800000)</span></span>  <br/> |<span data-ttu-id="fcde3-345">Un client peut obtenir la propriété **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** pour déterminer les caractéristiques d’une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="fcde3-345">A client can get the property **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** to determine the characteristic of a message store.</span></span> <span data-ttu-id="fcde3-346">Si le fournisseur de banque définit l’indicateur **STORE_PUSHER_OK** dans le masque de bits, ce qui signifie que le Gestionnaire de protocole MAPI ne sera pas analyser le magasin, et le magasin est responsable pour acheminer les modifications via les notifications à l’indexeur que les messages indexés.</span><span class="sxs-lookup"><span data-stu-id="fcde3-346">If the store provider sets the **STORE_PUSHER_OK** flag in the bitmask, that means the MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>  <br/> |
   
### <a name="definitions-for-namespaces"></a><span data-ttu-id="fcde3-347">Définitions pour les espaces de noms</span><span class="sxs-lookup"><span data-stu-id="fcde3-347">Definitions for namespaces</span></span>

<span data-ttu-id="fcde3-348">Les identificateurs globaux uniques (GUID) suivantes représentent les espaces de noms de propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="fcde3-348">The following globally unique identifiers (GUIDs) represent the namespaces of named properties.</span></span> <span data-ttu-id="fcde3-349">Ils sont indexés par le Gestionnaire de protocole MAPI (PH) et sont documentées en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fcde3-349">They are indexed by the MAPI Protocol Handler (PH), and are documented as read-only.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="fcde3-350">Les propriétés nommées ne doivent pas être utilisées pour créer ou modifier des éléments.</span><span class="sxs-lookup"><span data-stu-id="fcde3-350">The named properties should not be used to create or modify items.</span></span> 
  
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

#### <a name="mnidid-properties"></a><span data-ttu-id="fcde3-351">Propriétés MNID_ID</span><span class="sxs-lookup"><span data-stu-id="fcde3-351">MNID_ID Properties</span></span>
  
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

#### <a name="mnidstring-properties"></a><span data-ttu-id="fcde3-352">Propriétés MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="fcde3-352">MNID_STRING Properties</span></span>
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a><span data-ttu-id="fcde3-353">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="fcde3-353">Interface identifiers</span></span>

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

<span data-ttu-id="fcde3-354">Utiliser le `DEFINE_OLEGUID` macro définie dans le guiddef.h de fichier d’en-tête SDK Windows pour associer le nom symbolique GUID suivant à sa valeur.</span><span class="sxs-lookup"><span data-stu-id="fcde3-354">Use the  `DEFINE_OLEGUID` macro defined in the Windows SDK header file guiddef.h to associate the following GUID symbolic name with its value.</span></span> 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a><span data-ttu-id="fcde3-355">Constantes de carnet d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="fcde3-355">MAPI Address Book constants</span></span>

<span data-ttu-id="fcde3-356">Cette section contient les définitions des constantes pour le carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="fcde3-356">This section contains constant definitions for the MAPI Address Book.</span></span>
  
### <a name="constants"></a><span data-ttu-id="fcde3-357">Constantes</span><span class="sxs-lookup"><span data-stu-id="fcde3-357">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="fcde3-358">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="fcde3-358">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="fcde3-359">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="fcde3-359">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="fcde3-360">Le dossier racine d’un objet de carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="fcde3-360">The root folder for a MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="fcde3-361">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="fcde3-361">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="fcde3-362">((ULONG) 0 X 00000002)</span><span class="sxs-lookup"><span data-stu-id="fcde3-362">((ULONG) 0x00000002)</span></span>  <br/> |<span data-ttu-id="fcde3-363">Un sous-dossier contenu dans le dossier racine de l’objet de carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="fcde3-363">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="fcde3-364">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="fcde3-364">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="fcde3-365">((ULONG) 0 X 00000003)</span><span class="sxs-lookup"><span data-stu-id="fcde3-365">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="fcde3-366">Un objet conteneur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="fcde3-366">An address book container object.</span></span>  <br/> |
|<span data-ttu-id="fcde3-367">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="fcde3-367">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="fcde3-368">((ULONG) 0 X 00000004)</span><span class="sxs-lookup"><span data-stu-id="fcde3-368">((ULONG) 0x00000004)</span></span>  <br/> |<span data-ttu-id="fcde3-369">Un objet utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="fcde3-369">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="fcde3-370">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="fcde3-370">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="fcde3-371">((ULONG) 0 X 00000005)</span><span class="sxs-lookup"><span data-stu-id="fcde3-371">((ULONG) 0x00000005)</span></span>  <br/> |<span data-ttu-id="fcde3-372">Un objet de liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="fcde3-372">A distribution list object.</span></span>  <br/> |
   
## <a name="additional-mapi-constants"></a><span data-ttu-id="fcde3-373">Constantes MAPI supplémentaires</span><span class="sxs-lookup"><span data-stu-id="fcde3-373">Additional MAPI constants</span></span>

<span data-ttu-id="fcde3-374">Cette section contient des définitions de constantes, y compris les codes d’erreur et les identificateurs d’interface utilisés par l’API MAPI qui ont été n’a pas été exposées et documentées.</span><span class="sxs-lookup"><span data-stu-id="fcde3-374">This section contains constant definitions including error codes, and interface identifiers used by MAPI APIs that were not previously exposed and documented.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="fcde3-375">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="fcde3-375">DIALOG_MODAL</span></span>  <br/> |<span data-ttu-id="fcde3-376">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="fcde3-376">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="fcde3-377">Lorsqu’un client appelle la méthode [IAddrBook::Details](iaddrbook-details.md) , le client doit définir l’indicateur **DIALOG_MODAL** dans le paramètre _ulFlags_ pour afficher la boîte de dialogue modale affichant des informations détaillées sur une entrée de carnet d’adresses spécifique.</span><span class="sxs-lookup"><span data-stu-id="fcde3-377">When a client calls the [IAddrBook::Details](iaddrbook-details.md) method, the client must set the **DIALOG_MODAL** flag in the  _ulFlags_ parameter to display the modal dialog box showing the details about a particular address book entry.</span></span> <span data-ttu-id="fcde3-378">Cette constante est définie dans mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="fcde3-378">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="fcde3-379">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="fcde3-379">ITEMPROC_FORCE</span></span>  <br/> |<span data-ttu-id="fcde3-380">0x00000800</span><span class="sxs-lookup"><span data-stu-id="fcde3-380">0x00000800</span></span>  <br/> |<span data-ttu-id="fcde3-381">Dans Outlook 2007, encapsulé PST stocke des règles et filtrage du courrier indésirable traité sur les nouveaux messages avant que les clients MAPI sont avertis des nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="fcde3-381">In Outlook 2007, wrapped PST stores have rules and spam filtering processed on new messages before MAPI clients are notified of the new messages.</span></span> <span data-ttu-id="fcde3-382">Un fournisseur ou un client à l’aide de la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour créer un nouveau message dans des magasins PST doit définir l’indicateur **ITEMPROC_FORCE** dans le paramètre _ulFlags_ de la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour indiquer dans le fichier PST magasin que le message est éligible pour les règles de traitement avant que le magasin notifie n’importe quel client d’écoute de l’arrivée du nouveau message.</span><span class="sxs-lookup"><span data-stu-id="fcde3-382">A provider or client using the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new message in PST stores should set the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to indicate to the PST store that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="fcde3-383">Notez que ces règles de traitement seulement s’applique aux nouveaux messages créés sur un serveur qui n’est pas un serveur Microsoft Exchange, car Exchange Server traite les règles pour les messages sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="fcde3-383">Note that such rules processing only applies to new messages created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="fcde3-384">Par conséquent le fournisseur ou le client qui crée le message doit transmettre cet indicateur en combinaison avec **NON_EMS_XP_SAVE**, qui indique le serveur n’est pas un serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="fcde3-384">Hence the provider or client creating the message must pass this flag in combination with **NON_EMS_XP_SAVE**, which indicates the server is not an Exchange server.</span></span>  <br/> |
| <span data-ttu-id="fcde3-385">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="fcde3-385">MAPI_BG_SESSION</span></span>  <br/> |<span data-ttu-id="fcde3-386">0 x 00200000</span><span class="sxs-lookup"><span data-stu-id="fcde3-386">0x00200000</span></span>  <br/> |<span data-ttu-id="fcde3-387">Un client peut appeler la fonction [MAPILogonEx](mapilogonex.md) , définir l’indicateur **MAPI_BG_SESSION** dans le paramètre _flFlags_ se connecter à une session et effectuer des opérations en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="fcde3-387">A client can call the [MAPILogonEx](mapilogonex.md) function, setting the **MAPI_BG_SESSION** flag in the  _flFlags_ parameter to log on to a session and carry out any operations in the background.</span></span> <span data-ttu-id="fcde3-388">En règle générale, si un client a l’intention d’effectuer un traitement sur une thread d’arrière-plan ou dans un processus distinct d’une manière discrète à la thread de premier plan, il doit appeler [MAPILogonEx](mapilogonex.md) avec l’indicateur **MAPI_BG_SESSION** .</span><span class="sxs-lookup"><span data-stu-id="fcde3-388">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call [MAPILogonEx](mapilogonex.md) with the **MAPI_BG_SESSION** flag.</span></span> <span data-ttu-id="fcde3-389">Un exemple où il est utilisé est une application cliente, comme un moteur d’indexation, de l’ouverture d’un fichier de dossiers personnels (PST) pour l’accès de type d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="fcde3-389">An example where this is used is a client application, such as an indexing engine, opening a Personal Folders File (PST) for background type access.</span></span>  <br/> |
|<span data-ttu-id="fcde3-390">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="fcde3-390">MAPI_CACHE_ONLY</span></span>  <br/> |<span data-ttu-id="fcde3-391">0x00004000</span><span class="sxs-lookup"><span data-stu-id="fcde3-391">0x00004000</span></span>  <br/> |<span data-ttu-id="fcde3-392">Un client peut appeler la méthode [IAddrBook::OpenEntry](iaddrbook-openentry.md) , en définissant l’indicateur **MAPI_CACHE_ONLY** dans le paramètre _ulFlags_ pour ouvrir une entrée de carnet d’adresses et y accéder par la suite uniquement à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="fcde3-392">A client can call the [IAddrBook::OpenEntry](iaddrbook-openentry.md) method, setting the **MAPI_CACHE_ONLY** flag in the  _ulFlags_ parameter to open an address book entry and to access it subsequently only from the cache.</span></span> <span data-ttu-id="fcde3-393">Un exemple où il est utilisé est une application cliente qui souhaite ouvrir la liste d’adresses globale en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="fcde3-393">An example where this is used is a client application that wants to open the Global Address List in Cached Exchange mode and access an entry in that Address Book from the cache without creating traffic between the client and the server.</span></span>  <br/> |
|<span data-ttu-id="fcde3-394">MAPI_DIALOG_MODELESS</span><span class="sxs-lookup"><span data-stu-id="fcde3-394">MAPI_DIALOG_MODELESS</span></span>  <br/> |<span data-ttu-id="fcde3-395">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="fcde3-395">0x0000000C</span></span>  <br/> |<span data-ttu-id="fcde3-396">Cette valeur peut être passée à la fonction MAPISendMail Simple MAPI dans le paramètre _ulFlags_ pour spécifier qu’une boîte de dialogue non modale est affichée par l’application de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="fcde3-396">This value can be passed to the Simple MAPI MAPISendMail function in the  _ulFlags_ parameter to specify that a modeless dialog box is displayed by the default mail application.</span></span> <span data-ttu-id="fcde3-397">Si cet indicateur, ni MAPI_DIALOG (0 x 00000008) est définie, aucune boîte de dialogue ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="fcde3-397">If neither this flag nor MAPI_DIALOG (0x00000008) is set, no dialog box is displayed.</span></span>  <br/> |
|<span data-ttu-id="fcde3-398">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="fcde3-398">MAPI_NO_CACHE</span></span>  <br/> |<span data-ttu-id="fcde3-399">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="fcde3-399">0x00000200</span></span>  <br/> |<span data-ttu-id="fcde3-400">Si Microsoft Office Outlook est en Mode Exchange mis en cache et une banque a été ouvert en mode mis en cache, un client ou fournisseur de services peut appeler [IMsgStore::OpenEntry](imsgstore-openentry.md), définir l’indicateur **MAPI_NO_CACHE** dans le paramètre _ulFlags_ pour ouvrir un élément ou un dossier sur le magasin distant.</span><span class="sxs-lookup"><span data-stu-id="fcde3-400">If Microsoft Office Outlook is in Cached Exchange Mode and a store has been opened in cached mode, a client or service provider can call [IMsgStore::OpenEntry](imsgstore-openentry.md), setting the **MAPI_NO_CACHE** flag in the  _ulFlags_ parameter to open an item or a folder on the remote store.</span></span> <span data-ttu-id="fcde3-401">Notez que si vous ouvrez la banque de messages avec l’indicateur **MDB_ONLINE** sur le serveur distant, il est inutile d’utiliser l’indicateur **MAPI_NO_CACHE** .</span><span class="sxs-lookup"><span data-stu-id="fcde3-401">Note that if you open the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span>  <br/> |
|<span data-ttu-id="fcde3-402">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fcde3-402">MAPI_UNICODE</span></span>  <br/> |<span data-ttu-id="fcde3-403">0 x 80000000</span><span class="sxs-lookup"><span data-stu-id="fcde3-403">0x80000000</span></span>  <br/> |<span data-ttu-id="fcde3-404">Un client ou fournisseur de services peut appeler la fonction [OpenIMsgOnIStg](openimsgonistg.md) , définir l’indicateur **MAPI_UNICODE** dans le paramètre _ulFlags_ pour créer les fichiers .msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="fcde3-404">A client or service provider can call the [OpenIMsgOnIStg](openimsgonistg.md) function, setting the **MAPI_UNICODE** flag in the  _ulFlags_ parameter to create Unicode .msg files.</span></span> <span data-ttu-id="fcde3-405">Résultant [IMessage : IMAPIProp](imessageimapiprop.md) fichier affiche **STORE_UNICODE_OK** dans sa [Propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) et prend en charge les propriétés Unicode.</span><span class="sxs-lookup"><span data-stu-id="fcde3-405">The resulting [IMessage : IMAPIProp](imessageimapiprop.md) file shows **STORE_UNICODE_OK** in its [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> <span data-ttu-id="fcde3-406">Cette constante est définie dans mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="fcde3-406">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="fcde3-407">MDB_ONLINE</span><span class="sxs-lookup"><span data-stu-id="fcde3-407">MDB_ONLINE</span></span>  <br/> |<span data-ttu-id="fcde3-408">0 x 00000100</span><span class="sxs-lookup"><span data-stu-id="fcde3-408">0x00000100</span></span>  <br/> |<span data-ttu-id="fcde3-409">Si Outlook est en Mode Exchange mis en cache, un client ou fournisseur de services peut appeler la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) , définir l’indicateur **MDB_ONLINE** dans le paramètre _ulFlags_ pour remplacer la connexion à la banque de messages local et ouvrir la banque sur le serveur distant.</span><span class="sxs-lookup"><span data-stu-id="fcde3-409">If Outlook is in Cached Exchange Mode, a client or service provider can call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method, setting the **MDB_ONLINE** flag in the  _ulFlags_ parameter to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="fcde3-410">Notez que vous Impossible d’ouvrir une banque Exchange en mode mis en cache et en mode non mis en cache en même temps dans la même session MAPI.</span><span class="sxs-lookup"><span data-stu-id="fcde3-410">Note that you cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="fcde3-411">Si vous avez déjà ouvert la banque de messages mis en cache, vous devez soit fermer le magasin avant d’ouvrir avec cet indicateur ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d’informations Exchange sur le serveur distant à l’aide de cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="fcde3-411">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>  <br/> |
|<span data-ttu-id="fcde3-412">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="fcde3-412">NON_EMS_XP_SAVE</span></span>  <br/> |<span data-ttu-id="fcde3-413">0 x 00001000</span><span class="sxs-lookup"><span data-stu-id="fcde3-413">0x00001000</span></span>  <br/> |<span data-ttu-id="fcde3-414">Un client peut appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , en définissant l’indicateur **NON_EMS_XP_SAVE** dans le paramètre _ulFlags_ pour indiquer que le message n’a pas été remis à partir d’un serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="fcde3-414">A client can call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method, setting the **NON_EMS_XP_SAVE** flag in the  _ulFlags_ parameter to indicate that the message has not been delivered from an Exchange server.</span></span> <span data-ttu-id="fcde3-415">Cet indicateur doit être utilisé en combinaison avec l’indicateur **ITEMPROC_FORCE** dans le paramètre _ulFlags_ pour indiquer à une banque de dossiers personnels que le message est éligible pour les règles de transformation avant le fichier PST banque notifie n’importe quel client d’écoute de l’arrivée de la Message.</span><span class="sxs-lookup"><span data-stu-id="fcde3-415">This flag should be used in combination with the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter to indicate to a PST store that the message is eligible for rules processing before the PST store notifies any listening client of the arrival of the message.</span></span> <span data-ttu-id="fcde3-416">Cela les règles de traitement seulement s’applique aux nouveaux messages créés avec [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) sur un serveur qui n’est pas un serveur Exchange (dans ce cas le serveur Exchange est ont déjà traités règles dans le message).</span><span class="sxs-lookup"><span data-stu-id="fcde3-416">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange server (in which case the Exchange server would have already processed rules on the message).</span></span>  <br/> |
|<span data-ttu-id="fcde3-417">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="fcde3-417">SPAMFILTER_ONSAVE</span></span>  <br/> |<span data-ttu-id="fcde3-418">0x00000080</span><span class="sxs-lookup"><span data-stu-id="fcde3-418">0x00000080</span></span>  <br/> |<span data-ttu-id="fcde3-419">Un client peut appeler [IMAPIProp::SaveChanges](imapiprop-savechanges.md), définir l’indicateur **SPAMFILTER_ONSAVE** dans le paramètre _ulFlags_ pour activer le filtrage d’un message en cours d’enregistrement du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="fcde3-419">A client can call [IMAPIProp::SaveChanges](imapiprop-savechanges.md), setting the **SPAMFILTER_ONSAVE** flag in the  _ulFlags_ parameter to enable spam filtering on a message that is being saved.</span></span> <span data-ttu-id="fcde3-420">Prise en charge de filtrage du courrier indésirable est disponible uniquement si le type d’adresse de messagerie de l’expéditeur est SMTP Simple Mail Transfer Protocol (), et le message est enregistré dans un magasin d’un fichier de dossiers personnels (PST).</span><span class="sxs-lookup"><span data-stu-id="fcde3-420">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>  <br/> |
|<span data-ttu-id="fcde3-421">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="fcde3-421">STORE_ITEMPROC</span></span>  <br/> |<span data-ttu-id="fcde3-422">0 x 00200000</span><span class="sxs-lookup"><span data-stu-id="fcde3-422">0x00200000</span></span>  <br/> |<span data-ttu-id="fcde3-423">Si cet indicateur est défini dans la [Propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) d’une banque de dossiers personnels encapsulée, il indique que lorsqu’un nouveau message arrive dans le magasin, le magasin possède des règles et filtrage du courrier indésirable traitées séparément dans le message.</span><span class="sxs-lookup"><span data-stu-id="fcde3-423">If this flag is set in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) of a wrapped PST store, it indicates that when a new message arrives at the store, the store has rules and spam filtering processed on the message separately.</span></span> <span data-ttu-id="fcde3-424">Le magasin appelle ensuite [IMAPISupport::Notify](imapisupport-notify.md), **fnevNewMail** dans la structure [NOTIFICATION](notification.md) qui est transmise en tant que paramètre et passe les détails du nouveau message à un client d’écoute.</span><span class="sxs-lookup"><span data-stu-id="fcde3-424">The store then calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and passing the details of the new message to a listening client.</span></span> <span data-ttu-id="fcde3-425">Par la suite, lorsque le client d’écoute reçoit la notification, il ne traite pas de règles dans le message.</span><span class="sxs-lookup"><span data-stu-id="fcde3-425">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span>  <br/> |
|<span data-ttu-id="fcde3-426">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="fcde3-426">STORE_UNICODE_OK</span></span>  <br/> |<span data-ttu-id="fcde3-427">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="fcde3-427">0x00040000</span></span>  <br/> |<span data-ttu-id="fcde3-428">Si cet indicateur est inclus dans la [Propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), elle indique que la banque prend en charge le stockage Unicode.</span><span class="sxs-lookup"><span data-stu-id="fcde3-428">If this flag is included in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md), it indicates that the store supports Unicode storage.</span></span> <span data-ttu-id="fcde3-429">Un client peut rechercher la présence de l’indicateur à décider s’il convient de demander ou d’enregistrer les informations de Unicode dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="fcde3-429">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span>  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a><span data-ttu-id="fcde3-430">Définitions pour l’archivage des éléments dans un dossier</span><span class="sxs-lookup"><span data-stu-id="fcde3-430">Definitions for archiving items in a folder</span></span>

<span data-ttu-id="fcde3-431">Les définitions de constantes suivantes sont des valeurs utilisées pour définir la [Propriété canonique PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="fcde3-431">The following constant definitions are values used to set the [PidTagAgingGranularity Canonical Property](pidtagaginggranularity-canonical-property.md).</span></span>
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a><span data-ttu-id="fcde3-432">Définitions d’affichage des objets distants</span><span class="sxs-lookup"><span data-stu-id="fcde3-432">Definitions for displaying remote objects</span></span>

<span data-ttu-id="fcde3-433">Les définitions de constante et la macro suivantes sont pour l’affichage des objets distants.</span><span class="sxs-lookup"><span data-stu-id="fcde3-433">The following constant and macro definitions are for displaying remote objects.</span></span> <span data-ttu-id="fcde3-434">Pour plus d’informations, voir la [Propriété canonique PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="fcde3-434">For more information, see the [PidTagDisplayTypeEx Canonical Property](pidtagdisplaytypeex-canonical-property.md).</span></span>
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a><span data-ttu-id="fcde3-435">Définitions de carnet d’adresses Exchange et Message stockent les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="fcde3-435">Definitions for Exchange address book and Message store error codes</span></span>

<span data-ttu-id="fcde3-436">Le texte suivant contient des définitions des codes d’erreur pour le carnet d’adresses Exchange et la banque de messages, dont la fonctionnalité de reconnexion.</span><span class="sxs-lookup"><span data-stu-id="fcde3-436">The following contains error code definitions for the Exchange Address Book and Message Store, which have reconnection capability.</span></span> <span data-ttu-id="fcde3-437">Le dernier appel à un déconnecté (catalogue Global) peut entraîner l’erreur **MAPI_E_END_OF_SESSION** , qui doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="fcde3-437">The last call to a disconnected Global Catalog (GC) may result in the **MAPI_E_END_OF_SESSION** error, which would need to be retried.</span></span> 
  
<span data-ttu-id="fcde3-438">MAPI prend en charge la reconnexion d’Outlook à un serveur de catalogue global sans reconfiguration spéciale, mais d’autres erreurs codes peuvent être renvoyés au client.</span><span class="sxs-lookup"><span data-stu-id="fcde3-438">Outlook's MAPI supports reconnection to a GC server without special reconfiguration, but some other error codes can be returned to the client.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="fcde3-439">MAPI_E_END_OF_SESSION</span><span class="sxs-lookup"><span data-stu-id="fcde3-439">MAPI_E_END_OF_SESSION</span></span>  <br/> |<span data-ttu-id="fcde3-440">0x80040200</span><span class="sxs-lookup"><span data-stu-id="fcde3-440">0x80040200</span></span>  <br/> |<span data-ttu-id="fcde3-441">Retourné lorsqu’une connexion a été déconnectée.</span><span class="sxs-lookup"><span data-stu-id="fcde3-441">Returned when a connection has been disconnected.</span></span>  <br/> |
|<span data-ttu-id="fcde3-442">MAPI_E_RECONNECTED</span><span class="sxs-lookup"><span data-stu-id="fcde3-442">MAPI_E_RECONNECTED</span></span>  <br/> |<span data-ttu-id="fcde3-443">0 x 80040125</span><span class="sxs-lookup"><span data-stu-id="fcde3-443">0x80040125</span></span>  <br/> |<span data-ttu-id="fcde3-444">Renvoyé lorsque le jeton de connexion de l’appel de procédure distante (RPC) est obsolète.</span><span class="sxs-lookup"><span data-stu-id="fcde3-444">Returned when the Remote Procedure Call (RPC) connection token is out-of-date.</span></span> <span data-ttu-id="fcde3-445">Si le jeton de la transaction actuelle est différent du jeton de la connexion, cela signifie qu’il s’est reconnecté, afin que **MAPI_E_RECONNECTED** est retourné et peut être traitée comme **MAPI_E_END_OF_SESSION**.</span><span class="sxs-lookup"><span data-stu-id="fcde3-445">If the token of the current transaction is different from the token of the connection that means it has reconnected, so **MAPI_E_RECONNECTED** is returned and can be treated the same as **MAPI_E_END_OF_SESSION**.</span></span> <span data-ttu-id="fcde3-446">L’appel doit être relancée.</span><span class="sxs-lookup"><span data-stu-id="fcde3-446">The call should be retried.</span></span>  <br/> |
|<span data-ttu-id="fcde3-447">MAPI_E_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="fcde3-447">MAPI_E_OFFLINE</span></span>  <br/> |<span data-ttu-id="fcde3-448">0x80040126</span><span class="sxs-lookup"><span data-stu-id="fcde3-448">0x80040126</span></span>  <br/> |<span data-ttu-id="fcde3-449">Renvoyé lorsque la connexion est en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="fcde3-449">Returned when the connection is offline.</span></span> <span data-ttu-id="fcde3-450">En règle générale, cela signifie que quelque chose s’est produite dans l’environnement, telles que la défaillance du serveur ou de perte de connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="fcde3-450">Typically this means that something has occurred in the environment, such as server failure or loss of network connectivity.</span></span> <span data-ttu-id="fcde3-451">Cette erreur est susceptible de se produire lors de l’utilisation d’un mode mis en cache de profil et tente de contourner le cache pour communiquer avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="fcde3-451">This error is most likely to occur when using a cached mode profile and attempting to bypass the cache to communicate with the server.</span></span> <span data-ttu-id="fcde3-452">Si le cache n’a jamais pu initialement établir une connexion au serveur, il peut être à l’état en mode hors connexion dans lequel **MAPI_E_OFFLINE** pourrait exposer.</span><span class="sxs-lookup"><span data-stu-id="fcde3-452">If the cache was never able to initially establish a connection to the server, it may be in the offline state in which **MAPI_E_OFFLINE** could surface.</span></span>  <br/> |
   
<span data-ttu-id="fcde3-453">Aucune de ces deux erreurs s’afficheront dans tous les scénarios où ils apparaîtraient probablement à appliquer.</span><span class="sxs-lookup"><span data-stu-id="fcde3-453">Neither of the preceding two errors will be returned in all scenarios where they would likely appear to apply.</span></span> <span data-ttu-id="fcde3-454">Dans la plupart des cas, **MAPI\_E_NETWORK_ERROR** ou **MAPI_E_CALL_FAILED** seront retournés.</span><span class="sxs-lookup"><span data-stu-id="fcde3-454">In most cases, **MAPI\_E_NETWORK_ERROR** or **MAPI_E_CALL_FAILED** will be returned.</span></span> <span data-ttu-id="fcde3-455">Ne s’affiche à l’aide du téléchargement de [Microsoft Exchange Server MAPI Client et Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) .</span><span class="sxs-lookup"><span data-stu-id="fcde3-455">Neither will appear using the [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) download.</span></span> 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a><span data-ttu-id="fcde3-456">Définitions de boîte aux lettres du serveur Exchange mis en cache des quotas de mode</span><span class="sxs-lookup"><span data-stu-id="fcde3-456">Definitions for Exchange Server Mailbox cached mode quotas</span></span>

<span data-ttu-id="fcde3-457">Les définitions de constantes suivantes sont utilisées par Microsoft Outlook 2010 et Microsoft Outlook 2013 pour définir la version d’Exchange mis en cache les quotas de profils en mode qui sont équivalents aux quotas de boîte aux lettres Exchange dans le cas contraire disponibles uniquement avec un profil en ligne.</span><span class="sxs-lookup"><span data-stu-id="fcde3-457">The following constant definitions are used by Microsoft Outlook 2010 and Microsoft Outlook 2013 to set the Exchange cached mode profile quotas that are equivalent to the Exchange mailbox quotas otherwise available only with an online profile.</span></span>
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

<span data-ttu-id="fcde3-458">Ces propriétés correspondent aux leurs propriétés online correspondantes et contiennent les mêmes valeurs en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="fcde3-458">These properties map to their correspondent online properties and contain the same values in kilobytes.</span></span> <span data-ttu-id="fcde3-459">PR_QUOTA_WARNING mappe sur PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND à PR_QUOTA_PROHIBIT_SEND_QUOTA et PR_QUOTA_RECEIVE à PR_PROHIBIT_RECEIVE_QUOTA.</span><span class="sxs-lookup"><span data-stu-id="fcde3-459">PR_QUOTA_WARNING maps to PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND to PR_QUOTA_PROHIBIT_SEND_QUOTA, and PR_QUOTA_RECEIVE to PR_PROHIBIT_RECEIVE_QUOTA.</span></span>
  
### <a name="definitions-for-message-format"></a><span data-ttu-id="fcde3-460">Définitions de format de message</span><span class="sxs-lookup"><span data-stu-id="fcde3-460">Definitions for message format</span></span>

<span data-ttu-id="fcde3-461">Les définitions de constantes suivantes sont des valeurs qui sont utilisées pour définir la [Propriété canonique PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="fcde3-461">The following constant definitions are values that are used to set the [PidTagMessageEditorFormat Canonical Property](pidtagmessageeditorformat-canonical-property.md).</span></span>
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a><span data-ttu-id="fcde3-462">Définitions à l’aide de RPC sur HTTP</span><span class="sxs-lookup"><span data-stu-id="fcde3-462">Definitions for using RPC over HTTP</span></span>

<span data-ttu-id="fcde3-463">Consultez la rubrique de la [Propriété canonique PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) pour les définitions de constantes permet de définir la propriété en tant qu’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="fcde3-463">See the [PidTagRpcOverHttpFlags Canonical Property](pidtagrpcoverhttpflags-canonical-property.md) topic for constant definitions used as flags to set the property.</span></span> 
  
<span data-ttu-id="fcde3-464">Consultez la rubrique de la [Propriété canonique PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) pour les définitions de constantes utilisées pour définir la propriété.</span><span class="sxs-lookup"><span data-stu-id="fcde3-464">See the [PidTagRpcOverHttpProxyAuthScheme Canonical Property](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) topic for constant definitions used to set the property.</span></span> 
  
### <a name="identifiers"></a><span data-ttu-id="fcde3-465">Identificateurs</span><span class="sxs-lookup"><span data-stu-id="fcde3-465">Identifiers</span></span>

<span data-ttu-id="fcde3-466">Utiliser le `DEFINE_OLEGUID` macro définie dans le guiddef.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows pour associer les noms symboliques GUID suivants à leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="fcde3-466">Use the  `DEFINE_OLEGUID` macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the following GUID symbolic names with their values.</span></span> 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

<span data-ttu-id="fcde3-467">L’identificateur suivant concerne la section Capone de carnet d’adresses qui contient une propriété [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) efficacement désactive la valeur par défaut pour plusieurs boîtes aux lettres Exchange ([MultiEx](using-multiple-exchange-accounts.md)) conteneur spécifié par [SetDefaultDir](iaddrbook-setdefaultdir.md).</span><span class="sxs-lookup"><span data-stu-id="fcde3-467">The following Identifier is for the Capone Profile section of an Address Book, which in support of multiple Exchange ([MultiEx](using-multiple-exchange-accounts.md)) mailboxes contains a [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property that effectively turns off the default container specified by [SetDefaultDir](iaddrbook-setdefaultdir.md).</span></span>
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a><span data-ttu-id="fcde3-468">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="fcde3-468">Interface identifiers</span></span>

#### <a name="imapisync"></a><span data-ttu-id="fcde3-469">IMAPISync</span><span class="sxs-lookup"><span data-stu-id="fcde3-469">IMAPISync</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a><span data-ttu-id="fcde3-470">IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="fcde3-470">IMAPISyncProgressCallback</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a><span data-ttu-id="fcde3-471">IID_IContabAdmin</span><span class="sxs-lookup"><span data-stu-id="fcde3-471">IID_IContabAdmin</span></span>
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a><span data-ttu-id="fcde3-472">IID_IMAPISECUREMESSAGE</span><span class="sxs-lookup"><span data-stu-id="fcde3-472">IID_IMAPISECUREMESSAGE</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a><span data-ttu-id="fcde3-473">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="fcde3-473">IID_IMAPIGetSession</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a><span data-ttu-id="fcde3-474">Identificateurs d’interface Gestionnaire de remplacer des fichiers PST</span><span class="sxs-lookup"><span data-stu-id="fcde3-474">PST Override Handler interface identifiers</span></span>

#### <a name="iidipstoverridereq"></a><span data-ttu-id="fcde3-475">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="fcde3-475">IID_IPSTOVERRIDEREQ</span></span>
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a><span data-ttu-id="fcde3-476">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="fcde3-476">IID_IPSTOVERRIDE1</span></span>
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a><span data-ttu-id="fcde3-477">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcde3-477">See also</span></span>

- [<span data-ttu-id="fcde3-478">À propos des ajouts MAPI</span><span class="sxs-lookup"><span data-stu-id="fcde3-478">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="fcde3-479">À propos des propriétés nommées utilisées par Outlook</span><span class="sxs-lookup"><span data-stu-id="fcde3-479">About Named Properties Used by Outlook</span></span>](about-named-properties-used-by-outlook.md)
- [<span data-ttu-id="fcde3-480">Accès à un magasin sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="fcde3-480">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="fcde3-481">Ouvrir une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="fcde3-481">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="fcde3-482">Gérer un message dans un fichier OST sans appeler de synchronisation en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="fcde3-482">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

