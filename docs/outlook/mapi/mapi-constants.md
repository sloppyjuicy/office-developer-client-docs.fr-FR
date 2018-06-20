---
title: Constantes MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d6d6c55776c1379ec1dab0e9a6f7ef0943d2480e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784596"
---
# <a name="mapi-constants"></a><span data-ttu-id="b7040-103">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b7040-103">MAPI constants</span></span>

<span data-ttu-id="b7040-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7040-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7040-105">Cette rubrique contient des définitions de constantes, les déclarations d’interface MAPI et les identificateurs de classe et d’interface utilisés par les API de MAPI.</span><span class="sxs-lookup"><span data-stu-id="b7040-105">This topic contains constant definitions, MAPI interface declarations, and class and interface identifiers used by the MAPI APIs.</span></span>
  
## <a name="class-and-interface-identifiers"></a><span data-ttu-id="b7040-106">Identificateurs de classe et d’interface</span><span class="sxs-lookup"><span data-stu-id="b7040-106">Class and interface identifiers</span></span>

<span data-ttu-id="b7040-107">Utilisez la macro DEFINE_GUID définie dans le guiddef.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows pour associer les noms symboliques identificateur global unique (GUID) à leurs valeurs, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="b7040-107">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values, unless otherwise indicated.</span></span>
  
## <a name="attachment-security-conversion-api"></a><span data-ttu-id="b7040-108">Conversion de sécurité des pièces jointes API</span><span class="sxs-lookup"><span data-stu-id="b7040-108">Attachment security conversion API</span></span>

<span data-ttu-id="b7040-109">Cette section contient des définitions de constantes et les identificateurs d’interface de l’API de sécurité des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="b7040-109">This section contains constant definitions and interface identifiers for the Attachment Security API.</span></span>
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

<span data-ttu-id="b7040-110">Utilisez la macro MAPIMETHOD définie dans le mapidefs.h de fichier d’en-tête SDK Windows pour définir la fonction virtuelle pure **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span><span class="sxs-lookup"><span data-stu-id="b7040-110">Use the MAPIMETHOD macro defined in the Windows SDK header file mapidefs.h to define the pure virtual function **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span></span> 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

<span data-ttu-id="b7040-111">Utilisez la macro DECLARE_MAPI_INTERFACE_ définie dans le mapidefs.h de fichier d’en-tête SDK Windows pour définir la table de méthodes virtuelles pour **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="b7040-111">Use the DECLARE_MAPI_INTERFACE_ macro defined in the Windows SDK header file mapidefs.h to define the virtual method table for **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span></span> 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a><span data-ttu-id="b7040-112">Conversion MAPI MIME API</span><span class="sxs-lookup"><span data-stu-id="b7040-112">MAPI-MIME conversion API</span></span>

<span data-ttu-id="b7040-113">Cette section contient des définitions de constantes et les identificateurs de classe et l’interface de l’API de Conversion MAPI MIME.</span><span class="sxs-lookup"><span data-stu-id="b7040-113">This section contains constant definitions and class and interface identifiers for the MAPI-MIME Conversion API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="b7040-114">Constants</span><span class="sxs-lookup"><span data-stu-id="b7040-114">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7040-115">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="b7040-115">CCSF_SMTP</span></span>  <br/> |<span data-ttu-id="b7040-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="b7040-116">0x0002</span></span>  <br/> |
|<span data-ttu-id="b7040-117">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="b7040-117">CCSF_NOHEADERS</span></span>  <br/> |<span data-ttu-id="b7040-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="b7040-118">0x0004</span></span>  <br/> |
|<span data-ttu-id="b7040-119">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="b7040-119">CCSF_USE_TNEF</span></span>  <br/> | <span data-ttu-id="b7040-120">0x0010</span><span class="sxs-lookup"><span data-stu-id="b7040-120">0x0010</span></span>  <br/> |
|<span data-ttu-id="b7040-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="b7040-121">CCSF_INCLUDE_BCC</span></span>  <br/> |<span data-ttu-id="b7040-122">0 x 0020</span><span class="sxs-lookup"><span data-stu-id="b7040-122">0x0020</span></span>  <br/> |
|<span data-ttu-id="b7040-123">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="b7040-123">CCSF_8BITHEADERS</span></span>  <br/> | <span data-ttu-id="b7040-124">0x0040</span><span class="sxs-lookup"><span data-stu-id="b7040-124">0x0040</span></span>  <br/> |
|<span data-ttu-id="b7040-125">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="b7040-125">CCSF_USE_RTF</span></span>  <br/> |<span data-ttu-id="b7040-126">0 x 0080</span><span class="sxs-lookup"><span data-stu-id="b7040-126">0x0080</span></span>  <br/> |
|<span data-ttu-id="b7040-127">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="b7040-127">CCSF_PLAIN_TEXT_ONLY</span></span>  <br/> |<span data-ttu-id="b7040-128">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="b7040-128">0x1000</span></span>  <br/> |
|<span data-ttu-id="b7040-129">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="b7040-129">CCSF_NO_MSGID</span></span>  <br/> |<span data-ttu-id="b7040-130">0 x 4000</span><span class="sxs-lookup"><span data-stu-id="b7040-130">0x4000</span></span>  <br/> |
|<span data-ttu-id="b7040-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b7040-131">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="b7040-132">*Comme défini dans le fichier d’en-tête winerror.h Kit de développement logiciel (SDK) de Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="b7040-132">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="b7040-133">Identificateurs de classe</span><span class="sxs-lookup"><span data-stu-id="b7040-133">Class identifiers</span></span>

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a><span data-ttu-id="b7040-134">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="b7040-134">Interface identifiers</span></span>

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a><span data-ttu-id="b7040-135">État en mode hors connexion API</span><span class="sxs-lookup"><span data-stu-id="b7040-135">Offline State API</span></span>

<span data-ttu-id="b7040-136">Cette section contient des définitions de constantes et les identificateurs de classe et l’interface de l’API de l’état en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="b7040-136">This section contains constant definitions and class and interface identifiers for the Offline State API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="b7040-137">Constants</span><span class="sxs-lookup"><span data-stu-id="b7040-137">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7040-138">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b7040-138">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="b7040-139">*Comme défini dans le fichier d’en-tête winerror.h Kit de développement logiciel (SDK) de Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="b7040-139">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="b7040-140">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="b7040-140">E_NOINTERFACE</span></span>  <br/> | <span data-ttu-id="b7040-141">*Comme défini dans le fichier d’en-tête winerror.h (SDK) Windows*</span><span class="sxs-lookup"><span data-stu-id="b7040-141">*As defined in the Windows (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="b7040-142">MAPIOFFLINE_ADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="b7040-142">MAPIOFFLINE_ADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="b7040-143">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="b7040-143">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="b7040-144">MAPIOFFLINE_UNADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="b7040-144">MAPIOFFLINE_UNADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="b7040-145">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="b7040-145">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="b7040-146">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="b7040-146">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span></span>  <br/> |<span data-ttu-id="b7040-147">1</span><span class="sxs-lookup"><span data-stu-id="b7040-147">1</span></span>  <br/> |
|<span data-ttu-id="b7040-148">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="b7040-148">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="b7040-149">0 x 1</span><span class="sxs-lookup"><span data-stu-id="b7040-149">0x1</span></span>  <br/> |
|<span data-ttu-id="b7040-150">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="b7040-150">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="b7040-151">0 x 2</span><span class="sxs-lookup"><span data-stu-id="b7040-151">0x2</span></span>  <br/> |
|<span data-ttu-id="b7040-152">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="b7040-152">MAPIOFFLINE_FLAG_BLOCK</span></span>  <br/> |<span data-ttu-id="b7040-153">0 x 00002000</span><span class="sxs-lookup"><span data-stu-id="b7040-153">0x00002000</span></span>  <br/> |
|<span data-ttu-id="b7040-154">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="b7040-154">MAPIOFFLINE_FLAG_DEFAULT</span></span>  <br/> |<span data-ttu-id="b7040-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7040-155">0x00000000</span></span>  <br/> |
|<span data-ttu-id="b7040-156">MAPIOFFLINE_STATE_ALL</span><span class="sxs-lookup"><span data-stu-id="b7040-156">MAPIOFFLINE_STATE_ALL</span></span>  <br/> |<span data-ttu-id="b7040-157">0x003f037f</span><span class="sxs-lookup"><span data-stu-id="b7040-157">0x003f037f</span></span>  <br/> |
|<span data-ttu-id="b7040-158">**En ligne ou hors connexion**</span><span class="sxs-lookup"><span data-stu-id="b7040-158">**Online or offline**</span></span> <br/> ||
|<span data-ttu-id="b7040-159">MAPIOFFLINE_STATE_OFFLINE_MASK</span><span class="sxs-lookup"><span data-stu-id="b7040-159">MAPIOFFLINE_STATE_OFFLINE_MASK</span></span>  <br/> |<span data-ttu-id="b7040-160">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="b7040-160">0x00000003</span></span>  <br/> |
|<span data-ttu-id="b7040-161">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="b7040-161">MAPIOFFLINE_STATE_OFFLINE</span></span>  <br/> |<span data-ttu-id="b7040-162">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7040-162">0x00000001</span></span>  <br/> |
|<span data-ttu-id="b7040-163">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="b7040-163">MAPIOFFLINE_STATE_ONLINE</span></span>  <br/> |<span data-ttu-id="b7040-164">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b7040-164">0x00000002</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="b7040-165">Identificateurs de classe</span><span class="sxs-lookup"><span data-stu-id="b7040-165">Class identifiers</span></span>

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a><span data-ttu-id="b7040-166">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="b7040-166">Interface identifiers</span></span>

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

## <a name="outlook-named-properties"></a><span data-ttu-id="b7040-167">Outlook des propriétés nommée</span><span class="sxs-lookup"><span data-stu-id="b7040-167">Outlook named properties</span></span>

<span data-ttu-id="b7040-168">Cette section contient des définitions de constantes pour les propriétés nommées et leurs espaces de noms et des constantes connexes.</span><span class="sxs-lookup"><span data-stu-id="b7040-168">This section contains constant definitions for named properties and their namespaces, and other related constants.</span></span>
  
### <a name="definitions-for-named-properties"></a><span data-ttu-id="b7040-169">Définitions de propriétés nommées</span><span class="sxs-lookup"><span data-stu-id="b7040-169">Definitions for named properties</span></span>

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

### <a name="definitions-for-namespaces"></a><span data-ttu-id="b7040-170">Définitions pour les espaces de noms</span><span class="sxs-lookup"><span data-stu-id="b7040-170">Definitions for namespaces</span></span>

<span data-ttu-id="b7040-171">Les identificateurs globaux uniques (GUID) suivantes représentent les espaces de noms des propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="b7040-171">The following globally unique identifiers (GUIDs) represent the namespaces of the named properties.</span></span>
  
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

<span data-ttu-id="b7040-172">Reportez-vous à la section emplacement de stockage MAPI pour les définitions PSETID.</span><span class="sxs-lookup"><span data-stu-id="b7040-172">Refer to the section MAPI Store for the PSETID definitions.</span></span>
  
### <a name="other-constants"></a><span data-ttu-id="b7040-173">Autres constantes</span><span class="sxs-lookup"><span data-stu-id="b7040-173">Other constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7040-174">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="b7040-174">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="b7040-175">0xD000000</span><span class="sxs-lookup"><span data-stu-id="b7040-175">0xD000000</span></span>  <br/> |
|<span data-ttu-id="b7040-176">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="b7040-176">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="b7040-177">0x2000000</span><span class="sxs-lookup"><span data-stu-id="b7040-177">0x2000000</span></span>  <br/> |
|<span data-ttu-id="b7040-178">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="b7040-178">MNID_ID</span></span>  <br/> | <span data-ttu-id="b7040-179">*Comme défini dans le mapidefs.h de fichier d’en-tête.*</span><span class="sxs-lookup"><span data-stu-id="b7040-179">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="b7040-180">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="b7040-180">MNID_STRING</span></span>  <br/> | <span data-ttu-id="b7040-181">*Comme défini dans le mapidefs.h de fichier d’en-tête.*</span><span class="sxs-lookup"><span data-stu-id="b7040-181">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="b7040-182">mtgNone</span><span class="sxs-lookup"><span data-stu-id="b7040-182">mtgNone</span></span>  <br/> |<span data-ttu-id="b7040-183">0 x 0</span><span class="sxs-lookup"><span data-stu-id="b7040-183">0x0</span></span>  <br/> |
|<span data-ttu-id="b7040-184">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="b7040-184">mtgRequest</span></span>  <br/> |<span data-ttu-id="b7040-185">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7040-185">0x00000001</span></span>  <br/> |
|<span data-ttu-id="b7040-186">mtgFullUpdate</span><span class="sxs-lookup"><span data-stu-id="b7040-186">mtgFullUpdate</span></span>  <br/> |<span data-ttu-id="b7040-187">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-187">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-188">mtgInfoUpdate</span><span class="sxs-lookup"><span data-stu-id="b7040-188">mtgInfoUpdate</span></span>  <br/> |<span data-ttu-id="b7040-189">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="b7040-189">0x00020000</span></span>  <br/> |
|<span data-ttu-id="b7040-190">mtgOutofDate</span><span class="sxs-lookup"><span data-stu-id="b7040-190">mtgOutofDate</span></span>  <br/> |<span data-ttu-id="b7040-191">0 x 00080000</span><span class="sxs-lookup"><span data-stu-id="b7040-191">0x00080000</span></span>  <br/> |
|<span data-ttu-id="b7040-192">mtgDelegated</span><span class="sxs-lookup"><span data-stu-id="b7040-192">mtgDelegated</span></span>  <br/> |<span data-ttu-id="b7040-193">0 x 00100000</span><span class="sxs-lookup"><span data-stu-id="b7040-193">0x00100000</span></span>  <br/> |
   
## <a name="replication-api"></a><span data-ttu-id="b7040-194">API de réplication</span><span class="sxs-lookup"><span data-stu-id="b7040-194">Replication API</span></span>

<span data-ttu-id="b7040-195">Cette section contient des définitions de constantes, les déclarations d’interface MAPI et identificateurs de classe et d’interface pour l’API de réplication.</span><span class="sxs-lookup"><span data-stu-id="b7040-195">This section contains constant definitions, MAPI interface declarations, and class and interface identifiers for the Replication API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="b7040-196">Constants</span><span class="sxs-lookup"><span data-stu-id="b7040-196">Constants</span></span>

<span data-ttu-id="b7040-197">Vous trouverez ci-dessous une structure [MAPIUID](mapiuid.md) qui identifie un fournisseur de services MAPI :</span><span class="sxs-lookup"><span data-stu-id="b7040-197">The following is a [MAPIUID](mapiuid.md) structure identifying a MAPI service provider:</span></span> 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|<span data-ttu-id="b7040-198">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-198">DNH_OK</span></span>  <br/> |<span data-ttu-id="b7040-199">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-199">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-200">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-200">DNT_OK</span></span>  <br/> |<span data-ttu-id="b7040-201">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-201">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-202">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="b7040-202">HSF_LOCAL</span></span>  <br/> |<span data-ttu-id="b7040-203">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="b7040-203">0x00000008</span></span>  <br/> |
|<span data-ttu-id="b7040-204">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="b7040-204">HSF_COPYDESTRUCTIVE</span></span>  <br/> |<span data-ttu-id="b7040-205">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="b7040-205">0x00000010</span></span>  <br/> |
|<span data-ttu-id="b7040-206">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-206">HSF_OK</span></span>  <br/> |<span data-ttu-id="b7040-207">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-207">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-208">MDB_OST_LOGON_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b7040-208">MDB_OST_LOGON_UNICODE</span></span>  <br/> |<span data-ttu-id="b7040-209">((ULONG) 0X00000800)</span><span class="sxs-lookup"><span data-stu-id="b7040-209">((ULONG) 0x00000800)</span></span>  <br/> |
|<span data-ttu-id="b7040-210">MDB_OST_LOGON_ANSI</span><span class="sxs-lookup"><span data-stu-id="b7040-210">MDB_OST_LOGON_ANSI</span></span>  <br/> |<span data-ttu-id="b7040-211">((ULONG) 0 X 00001000)</span><span class="sxs-lookup"><span data-stu-id="b7040-211">((ULONG) 0x00001000)</span></span>  <br/> |
|<span data-ttu-id="b7040-212">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="b7040-212">SHOW_SOFT_DELETES</span></span>  <br/> |<span data-ttu-id="b7040-213">((ULONG) 0 X 00000002)</span><span class="sxs-lookup"><span data-stu-id="b7040-213">((ULONG) 0x00000002)</span></span>  <br/> |
|<span data-ttu-id="b7040-214">SS_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="b7040-214">SS_ACTIVE</span></span>  <br/> |<span data-ttu-id="b7040-215">0</span><span class="sxs-lookup"><span data-stu-id="b7040-215">0</span></span>  <br/> |
|<span data-ttu-id="b7040-216">SS_SUSPENDED</span><span class="sxs-lookup"><span data-stu-id="b7040-216">SS_SUSPENDED</span></span>  <br/> |<span data-ttu-id="b7040-217">1</span><span class="sxs-lookup"><span data-stu-id="b7040-217">1</span></span>  <br/> |
|<span data-ttu-id="b7040-218">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="b7040-218">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="b7040-219">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7040-219">0x00000001</span></span>  <br/> |
|<span data-ttu-id="b7040-220">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="b7040-220">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="b7040-221">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b7040-221">0x00000002</span></span>  <br/> |
|<span data-ttu-id="b7040-222">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="b7040-222">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="b7040-223">0 x 00000040</span><span class="sxs-lookup"><span data-stu-id="b7040-223">0x00000040</span></span>  <br/> |
|<span data-ttu-id="b7040-224">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="b7040-224">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="b7040-225">0x00000080</span><span class="sxs-lookup"><span data-stu-id="b7040-225">0x00000080</span></span>  <br/> |
|<span data-ttu-id="b7040-226">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="b7040-226">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="b7040-227">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="b7040-227">0x00000200</span></span>  <br/> |
|<span data-ttu-id="b7040-228">SYNC_BACKGROUND</span><span class="sxs-lookup"><span data-stu-id="b7040-228">SYNC_BACKGROUND</span></span>  <br/> |<span data-ttu-id="b7040-229">0 x 00001000</span><span class="sxs-lookup"><span data-stu-id="b7040-229">0x00001000</span></span>  <br/> |
|<span data-ttu-id="b7040-230">SYNC_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="b7040-230">SYNC_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="b7040-231">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="b7040-231">0x00020000</span></span>  <br/> |
|<span data-ttu-id="b7040-232">SYNC_HEADERS</span><span class="sxs-lookup"><span data-stu-id="b7040-232">SYNC_HEADERS</span></span>  <br/> |<span data-ttu-id="b7040-233">0x02000000</span><span class="sxs-lookup"><span data-stu-id="b7040-233">0x02000000</span></span>  <br/> |
|<span data-ttu-id="b7040-234">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-234">UPC_OK</span></span>  <br/> |<span data-ttu-id="b7040-235">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-235">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-236">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="b7040-236">UPD_ASSOC</span></span>  <br/> |<span data-ttu-id="b7040-237">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7040-237">0x00000001</span></span>  <br/> |
|<span data-ttu-id="b7040-238">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="b7040-238">UPD_MOV</span></span>  <br/> |<span data-ttu-id="b7040-239">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b7040-239">0x00000002</span></span>  <br/> |
|<span data-ttu-id="b7040-240">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-240">UPD_OK</span></span>  <br/> |<span data-ttu-id="b7040-241">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-241">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-242">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="b7040-242">UPD_MOVED</span></span>  <br/> |<span data-ttu-id="b7040-243">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="b7040-243">0x00020000</span></span>  <br/> |
|<span data-ttu-id="b7040-244">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="b7040-244">UPD_UPDATE</span></span>  <br/> |<span data-ttu-id="b7040-245">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="b7040-245">0x00040000</span></span>  <br/> |
|<span data-ttu-id="b7040-246">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="b7040-246">UPD_COMMIT</span></span>  <br/> |<span data-ttu-id="b7040-247">0 x 00080000</span><span class="sxs-lookup"><span data-stu-id="b7040-247">0x00080000</span></span>  <br/> |
|<span data-ttu-id="b7040-248">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="b7040-248">UPF_NEW</span></span>  <br/> |<span data-ttu-id="b7040-249">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7040-249">0x00000001</span></span>  <br/> |
|<span data-ttu-id="b7040-250">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="b7040-250">UPF_MOD_PARENT</span></span>  <br/> |<span data-ttu-id="b7040-251">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b7040-251">0x00000002</span></span>  <br/> |
|<span data-ttu-id="b7040-252">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="b7040-252">UPF_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="b7040-253">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="b7040-253">0x00000004</span></span>  <br/> |
|<span data-ttu-id="b7040-254">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="b7040-254">UPF_DEL</span></span>  <br/> |<span data-ttu-id="b7040-255">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="b7040-255">0x00000008</span></span>  <br/> |
|<span data-ttu-id="b7040-256">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-256">UPF_OK</span></span>  <br/> |<span data-ttu-id="b7040-257">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-257">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-258">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-258">UPH_OK</span></span>  <br/> |<span data-ttu-id="b7040-259">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-259">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-260">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="b7040-260">UPM_ASSOC</span></span>  <br/> |<span data-ttu-id="b7040-261">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7040-261">0x00000001</span></span>  <br/> |
|<span data-ttu-id="b7040-262">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="b7040-262">UPM_NEW</span></span>  <br/> |<span data-ttu-id="b7040-263">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b7040-263">0x00000002</span></span>  <br/> |
|<span data-ttu-id="b7040-264">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="b7040-264">UPM_MOV</span></span>  <br/> |<span data-ttu-id="b7040-265">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="b7040-265">0x00000004</span></span>  <br/> |
|<span data-ttu-id="b7040-266">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="b7040-266">UPM_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="b7040-267">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="b7040-267">0x00000008</span></span>  <br/> |
|<span data-ttu-id="b7040-268">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="b7040-268">UPM_HEADER</span></span>  <br/> |<span data-ttu-id="b7040-269">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="b7040-269">0x00000010</span></span>  <br/> |
|<span data-ttu-id="b7040-270">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-270">UPM_OK</span></span>  <br/> |<span data-ttu-id="b7040-271">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-271">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-272">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="b7040-272">UPM_MOVED</span></span>  <br/> |<span data-ttu-id="b7040-273">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="b7040-273">0x00020000</span></span>  <br/> |
|<span data-ttu-id="b7040-274">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="b7040-274">UPM_COMMIT</span></span>  <br/> |<span data-ttu-id="b7040-275">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="b7040-275">0x00040000</span></span>  <br/> |
|<span data-ttu-id="b7040-276">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="b7040-276">UPM_DELETE</span></span>  <br/> |<span data-ttu-id="b7040-277">0 x 00080000</span><span class="sxs-lookup"><span data-stu-id="b7040-277">0x00080000</span></span>  <br/> |
|<span data-ttu-id="b7040-278">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="b7040-278">UPM_SAVE</span></span>  <br/> |<span data-ttu-id="b7040-279">0 x 00100000</span><span class="sxs-lookup"><span data-stu-id="b7040-279">0x00100000</span></span>  <br/> |
|<span data-ttu-id="b7040-280">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="b7040-280">UPR_ASSOC</span></span>  <br/> |<span data-ttu-id="b7040-281">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7040-281">0x00000001</span></span>  <br/> |
|<span data-ttu-id="b7040-282">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="b7040-282">UPR_READ</span></span>  <br/> |<span data-ttu-id="b7040-283">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b7040-283">0x00000002</span></span>  <br/> |
|<span data-ttu-id="b7040-284">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-284">UPR_OK</span></span>  <br/> |<span data-ttu-id="b7040-285">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-285">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-286">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="b7040-286">UPR_COMMIT</span></span>  <br/> |<span data-ttu-id="b7040-287">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="b7040-287">0x00020000</span></span>  <br/> |
|<span data-ttu-id="b7040-288">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="b7040-288">UPS_UPLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="b7040-289">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7040-289">0x00000001</span></span>  <br/> |
|<span data-ttu-id="b7040-290">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="b7040-290">UPS_DNLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="b7040-291">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b7040-291">0x00000002</span></span>  <br/> |
|<span data-ttu-id="b7040-292">UPS_ONE_FOLDER</span><span class="sxs-lookup"><span data-stu-id="b7040-292">UPS_ONE_FOLDER</span></span>  <br/> |<span data-ttu-id="b7040-293">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="b7040-293">0x00000004</span></span>  <br/> |
|<span data-ttu-id="b7040-294">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="b7040-294">UPS_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="b7040-295">0x00000080</span><span class="sxs-lookup"><span data-stu-id="b7040-295">0x00000080</span></span>  <br/> |
|<span data-ttu-id="b7040-296">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-296">UPS_OK</span></span>  <br/> |<span data-ttu-id="b7040-297">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-297">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-298">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-298">UPT_OK</span></span>  <br/> |<span data-ttu-id="b7040-299">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-299">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-300">UPT_PUBLIC</span><span class="sxs-lookup"><span data-stu-id="b7040-300">UPT_PUBLIC</span></span>  <br/> |<span data-ttu-id="b7040-301">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7040-301">0x00000001</span></span>  <br/> |
|<span data-ttu-id="b7040-302">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="b7040-302">UPV_ERROR</span></span>  <br/> |<span data-ttu-id="b7040-303">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="b7040-303">0x00010000</span></span>  <br/> |
|<span data-ttu-id="b7040-304">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="b7040-304">UPV_DIRTY</span></span>  <br/> |<span data-ttu-id="b7040-305">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="b7040-305">0x00020000</span></span>  <br/> |
|<span data-ttu-id="b7040-306">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="b7040-306">UPV_COMMIT</span></span>  <br/> |<span data-ttu-id="b7040-307">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="b7040-307">0x00040000</span></span>  <br/> |
   
### <a name="interface-declarations"></a><span data-ttu-id="b7040-308">Déclarations d’interface</span><span class="sxs-lookup"><span data-stu-id="b7040-308">Interface declarations</span></span>

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a><span data-ttu-id="b7040-309">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="b7040-309">Interface identifiers</span></span>

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

<span data-ttu-id="b7040-310">Utilisez les deux identificateurs d’interface suivant avec [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md)ou [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir et ignorer tout fournisseur de contrôle sur un objet folder et un objet de message, respectivement.</span><span class="sxs-lookup"><span data-stu-id="b7040-310">Use the two following interface identifiers with [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), or [IMsgStore::OpenEntry](imsgstore-openentry.md) to open and ignore any provider check on a folder object and a message object, respectively.</span></span> 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a><span data-ttu-id="b7040-311">Emplacement de stockage MAPI</span><span class="sxs-lookup"><span data-stu-id="b7040-311">MAPI store</span></span>

<span data-ttu-id="b7040-312">Cette section contient des définitions de constantes et identificateurs d’interface utilisé par les API de cette interface avec un magasin MAPI.</span><span class="sxs-lookup"><span data-stu-id="b7040-312">This section contains constant definitions and interface identifiers used by APIs that interface with a MAPI store.</span></span>
  
### <a name="constants"></a><span data-ttu-id="b7040-313">Constants</span><span class="sxs-lookup"><span data-stu-id="b7040-313">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="b7040-314">fnevIndexing</span><span class="sxs-lookup"><span data-stu-id="b7040-314">fnevIndexing</span></span>  <br/> |<span data-ttu-id="b7040-315">((ULONG) 0 X 00010000)</span><span class="sxs-lookup"><span data-stu-id="b7040-315">((ULONG) 0x00010000)</span></span>  <br/> |<span data-ttu-id="b7040-316">Un fournisseur de magasins peut spécifier **fnevIndexing** dans le membre **ulEventType** de la structure de **[NOTIFICATION](notification.md)** pour signaler l’indexeur qu’un objet est prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="b7040-316">A store provider can specify **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure to notify the indexer that an object is ready for indexing.</span></span> <span data-ttu-id="b7040-317">Membre de la structure de **NOTIFICATION** **info** contient une structure **[EXTENDED_NOTIFICATION](extended_notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="b7040-317">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="b7040-318">FS_NONE</span><span class="sxs-lookup"><span data-stu-id="b7040-318">FS_NONE</span></span>  <br/> |<span data-ttu-id="b7040-319">0 x 00</span><span class="sxs-lookup"><span data-stu-id="b7040-319">0x00</span></span>  <br/> |<span data-ttu-id="b7040-320">Un client peut appeler **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** et vérification pour le masque de bits retournée.</span><span class="sxs-lookup"><span data-stu-id="b7040-320">A client can call **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** and check for the returned bitmask.</span></span> <span data-ttu-id="b7040-321">**FS_NONE** indique que le dossier ne prend pas en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="b7040-321">**FS_NONE** indicates that the folder does not support sharing.</span></span>  <br/> |
|<span data-ttu-id="b7040-322">FS_SUPPORTS_SHARING</span><span class="sxs-lookup"><span data-stu-id="b7040-322">FS_SUPPORTS_SHARING</span></span>  <br/> |<span data-ttu-id="b7040-323">0 x 01</span><span class="sxs-lookup"><span data-stu-id="b7040-323">0x01</span></span>  <br/> |<span data-ttu-id="b7040-324">Un client peut appeler **IFolderSupport::GetSupportMask** et vérification pour le masque de bits retournée.</span><span class="sxs-lookup"><span data-stu-id="b7040-324">A client can call **IFolderSupport::GetSupportMask** and check for the returned bitmask.</span></span> <span data-ttu-id="b7040-325">**FS_SUPPORTS_SHARING** indique que le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="b7040-325">**FS_SUPPORTS_SHARING** indicates that the folder supports sharing.</span></span>  <br/> |
|<span data-ttu-id="b7040-326">INDEXING_SEARCH_OWNER</span><span class="sxs-lookup"><span data-stu-id="b7040-326">INDEXING_SEARCH_OWNER</span></span>  <br/> |<span data-ttu-id="b7040-327">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="b7040-327">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="b7040-328">Identifie le processus qui est envoi une notification à un indexeur qu’un objet est prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="b7040-328">Identifies the process that is pushing a notification to an indexer that an object is ready for indexing.</span></span>  <br/> |
|<span data-ttu-id="b7040-329">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="b7040-329">MNID_ID</span></span>  <br/> |<span data-ttu-id="b7040-330">Comme défini dans le mapidefs.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="b7040-330">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h</span></span>  <br/> |<span data-ttu-id="b7040-331">Une valeur pour le champ **ulKind** de la structure **[MAPINAMEID](mapinameid.md)** .</span><span class="sxs-lookup"><span data-stu-id="b7040-331">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="b7040-332">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="b7040-332">MNID_STRING</span></span>  <br/> |<span data-ttu-id="b7040-333">Comme défini dans le mapidefs.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b7040-333">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h.</span></span>  <br/> |<span data-ttu-id="b7040-334">Une valeur pour le champ **ulKind** de la structure **[MAPINAMEID](mapinameid.md)** .</span><span class="sxs-lookup"><span data-stu-id="b7040-334">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="b7040-335">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="b7040-335">MSCAP_RES_ANNOTATION</span></span>  <br/> |<span data-ttu-id="b7040-336">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="b7040-336">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="b7040-337">Si un client spécifie **MSCAP_SEL_RESTRICTION** en *mscapSelector* de **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** peut renvoyer cette valeur si la banque ignore les paramètres non valides dans une restriction.</span><span class="sxs-lookup"><span data-stu-id="b7040-337">If a client specifies **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  for **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** can return this value if the store ignores invalid parameters in a restriction.</span></span>  <br/> |
|<span data-ttu-id="b7040-338">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="b7040-338">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>  <br/> |<span data-ttu-id="b7040-339">((ULONG) 0 X 00000020)</span><span class="sxs-lookup"><span data-stu-id="b7040-339">((ULONG) 0x00000020)</span></span>  <br/> |<span data-ttu-id="b7040-340">Si un client spécifie **MSCAP_SEL_FOLDER** en *mscapSelector* de **IMSCapabilities::GetCapabilities**, **GetCapabilities** peut renvoyer cette valeur si le magasin est un magasin par défaut qui prend en charge les pages d’accueil du dossier.</span><span class="sxs-lookup"><span data-stu-id="b7040-340">If a client specifies **MSCAP_SEL_FOLDER** in  *mscapSelector*  for **IMSCapabilities::GetCapabilities**, **GetCapabilities** can return this value if the store is a non-default store that supports folder home pages.</span></span>  <br/> |
|<span data-ttu-id="b7040-341">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-341">STORE_PUSHER_OK</span></span>  <br/> |<span data-ttu-id="b7040-342">((ULONG) 0 X 00800000)</span><span class="sxs-lookup"><span data-stu-id="b7040-342">((ULONG) 0x00800000)</span></span>  <br/> |<span data-ttu-id="b7040-343">Un client peut obtenir la propriété **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** pour déterminer les caractéristiques d’une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="b7040-343">A client can get the property **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** to determine the characteristic of a message store.</span></span> <span data-ttu-id="b7040-344">Si le fournisseur de banque définit l’indicateur **STORE_PUSHER_OK** dans le masque de bits, ce qui signifie que le Gestionnaire de protocole MAPI ne sera pas analyser le magasin, et le magasin est responsable pour acheminer les modifications via les notifications à l’indexeur que les messages indexés.</span><span class="sxs-lookup"><span data-stu-id="b7040-344">If the store provider sets the **STORE_PUSHER_OK** flag in the bitmask, that means the MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>  <br/> |
   
### <a name="definitions-for-namespaces"></a><span data-ttu-id="b7040-345">Définitions pour les espaces de noms</span><span class="sxs-lookup"><span data-stu-id="b7040-345">Definitions for namespaces</span></span>

<span data-ttu-id="b7040-346">Les identificateurs globaux uniques (GUID) suivantes représentent les espaces de noms de propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="b7040-346">The following globally unique identifiers (GUIDs) represent the namespaces of named properties.</span></span> <span data-ttu-id="b7040-347">Ils sont indexés par le Gestionnaire de protocole MAPI (PH) et sont documentées en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b7040-347">They are indexed by the MAPI Protocol Handler (PH), and are documented as read-only.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="b7040-348">Les propriétés nommées ne doivent pas être utilisées pour créer ou modifier des éléments.</span><span class="sxs-lookup"><span data-stu-id="b7040-348">The named properties should not be used to create or modify items.</span></span> 
  
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

#### <a name="mnidid-properties"></a><span data-ttu-id="b7040-349">Propriétés MNID_ID</span><span class="sxs-lookup"><span data-stu-id="b7040-349">MNID_ID Properties</span></span>
  
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

#### <a name="mnidstring-properties"></a><span data-ttu-id="b7040-350">Propriétés MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="b7040-350">MNID_STRING Properties</span></span>
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a><span data-ttu-id="b7040-351">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="b7040-351">Interface identifiers</span></span>

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

<span data-ttu-id="b7040-352">Utiliser le `DEFINE_OLEGUID` macro définie dans le guiddef.h de fichier d’en-tête SDK Windows pour associer le nom symbolique GUID suivant à sa valeur.</span><span class="sxs-lookup"><span data-stu-id="b7040-352">Use the  `DEFINE_OLEGUID` macro defined in the Windows SDK header file guiddef.h to associate the following GUID symbolic name with its value.</span></span> 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a><span data-ttu-id="b7040-353">Constantes de carnet d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="b7040-353">MAPI Address Book constants</span></span>

<span data-ttu-id="b7040-354">Cette section contient les définitions des constantes pour le carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="b7040-354">This section contains constant definitions for the MAPI Address Book.</span></span>
  
### <a name="constants"></a><span data-ttu-id="b7040-355">Constants</span><span class="sxs-lookup"><span data-stu-id="b7040-355">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="b7040-356">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="b7040-356">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="b7040-357">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="b7040-357">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="b7040-358">Le dossier racine d’un objet de carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="b7040-358">The root folder for a MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="b7040-359">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="b7040-359">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="b7040-360">((ULONG) 0 X 00000002)</span><span class="sxs-lookup"><span data-stu-id="b7040-360">((ULONG) 0x00000002)</span></span>  <br/> |<span data-ttu-id="b7040-361">Un sous-dossier contenu dans le dossier racine de l’objet de carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="b7040-361">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="b7040-362">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="b7040-362">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="b7040-363">((ULONG) 0 X 00000003)</span><span class="sxs-lookup"><span data-stu-id="b7040-363">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="b7040-364">Un objet conteneur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="b7040-364">An address book container object.</span></span>  <br/> |
|<span data-ttu-id="b7040-365">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="b7040-365">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="b7040-366">((ULONG) 0 X 00000004)</span><span class="sxs-lookup"><span data-stu-id="b7040-366">((ULONG) 0x00000004)</span></span>  <br/> |<span data-ttu-id="b7040-367">Un objet utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b7040-367">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="b7040-368">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b7040-368">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="b7040-369">((ULONG) 0 X 00000005)</span><span class="sxs-lookup"><span data-stu-id="b7040-369">((ULONG) 0x00000005)</span></span>  <br/> |<span data-ttu-id="b7040-370">Un objet de liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="b7040-370">A distribution list object.</span></span>  <br/> |
   
## <a name="additional-mapi-constants"></a><span data-ttu-id="b7040-371">Constantes MAPI supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b7040-371">Additional MAPI constants</span></span>

<span data-ttu-id="b7040-372">Cette section contient des définitions de constantes, y compris les codes d’erreur et les identificateurs d’interface utilisés par l’API MAPI qui ont été n’a pas été exposées et documentées.</span><span class="sxs-lookup"><span data-stu-id="b7040-372">This section contains constant definitions including error codes, and interface identifiers used by MAPI APIs that were not previously exposed and documented.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="b7040-373">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="b7040-373">DIALOG_MODAL</span></span>  <br/> |<span data-ttu-id="b7040-374">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="b7040-374">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="b7040-375">Lorsqu’un client appelle la méthode [IAddrBook::Details](iaddrbook-details.md) , le client doit définir l’indicateur **DIALOG_MODAL** dans le paramètre _ulFlags_ pour afficher la boîte de dialogue modale affichant des informations détaillées sur une entrée de carnet d’adresses spécifique.</span><span class="sxs-lookup"><span data-stu-id="b7040-375">When a client calls the [IAddrBook::Details](iaddrbook-details.md) method, the client must set the **DIALOG_MODAL** flag in the  _ulFlags_ parameter to display the modal dialog box showing the details about a particular address book entry.</span></span> <span data-ttu-id="b7040-376">Cette constante est définie dans mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="b7040-376">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="b7040-377">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="b7040-377">ITEMPROC_FORCE</span></span>  <br/> |<span data-ttu-id="b7040-378">0x00000800</span><span class="sxs-lookup"><span data-stu-id="b7040-378">0x00000800</span></span>  <br/> |<span data-ttu-id="b7040-379">Dans Outlook 2007, encapsulé PST stocke des règles et filtrage du courrier indésirable traité sur les nouveaux messages avant que les clients MAPI sont avertis des nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="b7040-379">In Outlook 2007, wrapped PST stores have rules and spam filtering processed on new messages before MAPI clients are notified of the new messages.</span></span> <span data-ttu-id="b7040-380">Un fournisseur ou un client à l’aide de la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour créer un nouveau message dans des magasins PST doit définir l’indicateur **ITEMPROC_FORCE** dans le paramètre _ulFlags_ de la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour indiquer dans le fichier PST magasin que le message est éligible pour les règles de traitement avant que le magasin notifie n’importe quel client d’écoute de l’arrivée du nouveau message.</span><span class="sxs-lookup"><span data-stu-id="b7040-380">A provider or client using the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new message in PST stores should set the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to indicate to the PST store that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="b7040-381">Notez que ces règles de traitement seulement s’applique aux nouveaux messages créés sur un serveur qui n’est pas un serveur Microsoft Exchange, car Exchange Server traite les règles pour les messages sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="b7040-381">Note that such rules processing only applies to new messages created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="b7040-382">Par conséquent le fournisseur ou le client qui crée le message doit transmettre cet indicateur en combinaison avec **NON_EMS_XP_SAVE**, qui indique le serveur n’est pas un serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="b7040-382">Hence the provider or client creating the message must pass this flag in combination with **NON_EMS_XP_SAVE**, which indicates the server is not an Exchange server.</span></span>  <br/> |
| <span data-ttu-id="b7040-383">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="b7040-383">MAPI_BG_SESSION</span></span>  <br/> |<span data-ttu-id="b7040-384">0 x 00200000</span><span class="sxs-lookup"><span data-stu-id="b7040-384">0x00200000</span></span>  <br/> |<span data-ttu-id="b7040-385">Un client peut appeler la fonction [MAPILogonEx](mapilogonex.md) , définir l’indicateur **MAPI_BG_SESSION** dans le paramètre _flFlags_ se connecter à une session et effectuer des opérations en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b7040-385">A client can call the [MAPILogonEx](mapilogonex.md) function, setting the **MAPI_BG_SESSION** flag in the  _flFlags_ parameter to log on to a session and carry out any operations in the background.</span></span> <span data-ttu-id="b7040-386">En règle générale, si un client a l’intention d’effectuer un traitement sur une thread d’arrière-plan ou dans un processus distinct d’une manière discrète à la thread de premier plan, il doit appeler [MAPILogonEx](mapilogonex.md) avec l’indicateur **MAPI_BG_SESSION** .</span><span class="sxs-lookup"><span data-stu-id="b7040-386">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call [MAPILogonEx](mapilogonex.md) with the **MAPI_BG_SESSION** flag.</span></span> <span data-ttu-id="b7040-387">Un exemple où il est utilisé est une application cliente, comme un moteur d’indexation, de l’ouverture d’un fichier de dossiers personnels (PST) pour l’accès de type d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b7040-387">An example where this is used is a client application, such as an indexing engine, opening a Personal Folders File (PST) for background type access.</span></span>  <br/> |
|<span data-ttu-id="b7040-388">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="b7040-388">MAPI_CACHE_ONLY</span></span>  <br/> |<span data-ttu-id="b7040-389">0x00004000</span><span class="sxs-lookup"><span data-stu-id="b7040-389">0x00004000</span></span>  <br/> |<span data-ttu-id="b7040-390">Un client peut appeler la méthode [IAddrBook::OpenEntry](iaddrbook-openentry.md) , en définissant l’indicateur **MAPI_CACHE_ONLY** dans le paramètre _ulFlags_ pour ouvrir une entrée de carnet d’adresses et y accéder par la suite uniquement à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="b7040-390">A client can call the [IAddrBook::OpenEntry](iaddrbook-openentry.md) method, setting the **MAPI_CACHE_ONLY** flag in the  _ulFlags_ parameter to open an address book entry and to access it subsequently only from the cache.</span></span> <span data-ttu-id="b7040-391">Un exemple où il est utilisé est une application cliente qui souhaite ouvrir la liste d’adresses globale en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="b7040-391">An example where this is used is a client application that wants to open the Global Address List in Cached Exchange mode and access an entry in that Address Book from the cache without creating traffic between the client and the server.</span></span>  <br/> |
|<span data-ttu-id="b7040-392">MAPI_DIALOG_MODELESS</span><span class="sxs-lookup"><span data-stu-id="b7040-392">MAPI_DIALOG_MODELESS</span></span>  <br/> |<span data-ttu-id="b7040-393">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="b7040-393">0x0000000C</span></span>  <br/> |<span data-ttu-id="b7040-394">Cette valeur peut être passée à la fonction MAPISendMail Simple MAPI dans le paramètre _ulFlags_ pour spécifier qu’une boîte de dialogue non modale est affichée par l’application de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="b7040-394">This value can be passed to the Simple MAPI MAPISendMail function in the  _ulFlags_ parameter to specify that a modeless dialog box is displayed by the default mail application.</span></span> <span data-ttu-id="b7040-395">Si cet indicateur, ni MAPI_DIALOG (0 x 00000008) est définie, aucune boîte de dialogue ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b7040-395">If neither this flag nor MAPI_DIALOG (0x00000008) is set, no dialog box is displayed.</span></span>  <br/> |
|<span data-ttu-id="b7040-396">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="b7040-396">MAPI_NO_CACHE</span></span>  <br/> |<span data-ttu-id="b7040-397">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="b7040-397">0x00000200</span></span>  <br/> |<span data-ttu-id="b7040-398">Si Microsoft Office Outlook est en Mode Exchange mis en cache et une banque a été ouvert en mode mis en cache, un client ou fournisseur de services peut appeler [IMsgStore::OpenEntry](imsgstore-openentry.md), définir l’indicateur **MAPI_NO_CACHE** dans le paramètre _ulFlags_ pour ouvrir un élément ou un dossier sur le magasin distant.</span><span class="sxs-lookup"><span data-stu-id="b7040-398">If Microsoft Office Outlook is in Cached Exchange Mode and a store has been opened in cached mode, a client or service provider can call [IMsgStore::OpenEntry](imsgstore-openentry.md), setting the **MAPI_NO_CACHE** flag in the  _ulFlags_ parameter to open an item or a folder on the remote store.</span></span> <span data-ttu-id="b7040-399">Notez que si vous ouvrez la banque de messages avec l’indicateur **MDB_ONLINE** sur le serveur distant, il est inutile d’utiliser l’indicateur **MAPI_NO_CACHE** .</span><span class="sxs-lookup"><span data-stu-id="b7040-399">Note that if you open the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span>  <br/> |
|<span data-ttu-id="b7040-400">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b7040-400">MAPI_UNICODE</span></span>  <br/> |<span data-ttu-id="b7040-401">0 x 80000000</span><span class="sxs-lookup"><span data-stu-id="b7040-401">0x80000000</span></span>  <br/> |<span data-ttu-id="b7040-402">Un client ou fournisseur de services peut appeler la fonction [OpenIMsgOnIStg](openimsgonistg.md) , définir l’indicateur **MAPI_UNICODE** dans le paramètre _ulFlags_ pour créer les fichiers .msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="b7040-402">A client or service provider can call the [OpenIMsgOnIStg](openimsgonistg.md) function, setting the **MAPI_UNICODE** flag in the  _ulFlags_ parameter to create Unicode .msg files.</span></span> <span data-ttu-id="b7040-403">Résultant [IMessage : IMAPIProp](imessageimapiprop.md) fichier affiche **STORE_UNICODE_OK** dans sa [Propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) et prend en charge les propriétés Unicode.</span><span class="sxs-lookup"><span data-stu-id="b7040-403">The resulting [IMessage : IMAPIProp](imessageimapiprop.md) file shows **STORE_UNICODE_OK** in its [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> <span data-ttu-id="b7040-404">Cette constante est définie dans mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="b7040-404">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="b7040-405">MDB_ONLINE</span><span class="sxs-lookup"><span data-stu-id="b7040-405">MDB_ONLINE</span></span>  <br/> |<span data-ttu-id="b7040-406">0 x 00000100</span><span class="sxs-lookup"><span data-stu-id="b7040-406">0x00000100</span></span>  <br/> |<span data-ttu-id="b7040-407">Si Outlook est en Mode Exchange mis en cache, un client ou fournisseur de services peut appeler la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) , définir l’indicateur **MDB_ONLINE** dans le paramètre _ulFlags_ pour remplacer la connexion à la banque de messages local et ouvrir la banque sur le serveur distant.</span><span class="sxs-lookup"><span data-stu-id="b7040-407">If Outlook is in Cached Exchange Mode, a client or service provider can call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method, setting the **MDB_ONLINE** flag in the  _ulFlags_ parameter to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="b7040-408">Notez que vous Impossible d’ouvrir une banque Exchange en mode mis en cache et en mode non mis en cache en même temps dans la même session MAPI.</span><span class="sxs-lookup"><span data-stu-id="b7040-408">Note that you cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="b7040-409">Si vous avez déjà ouvert la banque de messages mis en cache, vous devez soit fermer le magasin avant d’ouvrir avec cet indicateur ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d’informations Exchange sur le serveur distant à l’aide de cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="b7040-409">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>  <br/> |
|<span data-ttu-id="b7040-410">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="b7040-410">NON_EMS_XP_SAVE</span></span>  <br/> |<span data-ttu-id="b7040-411">0 x 00001000</span><span class="sxs-lookup"><span data-stu-id="b7040-411">0x00001000</span></span>  <br/> |<span data-ttu-id="b7040-412">Un client peut appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , en définissant l’indicateur **NON_EMS_XP_SAVE** dans le paramètre _ulFlags_ pour indiquer que le message n’a pas été remis à partir d’un serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="b7040-412">A client can call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method, setting the **NON_EMS_XP_SAVE** flag in the  _ulFlags_ parameter to indicate that the message has not been delivered from an Exchange server.</span></span> <span data-ttu-id="b7040-413">Cet indicateur doit être utilisé en combinaison avec l’indicateur **ITEMPROC_FORCE** dans le paramètre _ulFlags_ pour indiquer à une banque de dossiers personnels que le message est éligible pour les règles de transformation avant le fichier PST banque notifie n’importe quel client d’écoute de l’arrivée de la Message.</span><span class="sxs-lookup"><span data-stu-id="b7040-413">This flag should be used in combination with the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter to indicate to a PST store that the message is eligible for rules processing before the PST store notifies any listening client of the arrival of the message.</span></span> <span data-ttu-id="b7040-414">Cela les règles de traitement seulement s’applique aux nouveaux messages créés avec [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) sur un serveur qui n’est pas un serveur Exchange (dans ce cas le serveur Exchange est ont déjà traités règles dans le message).</span><span class="sxs-lookup"><span data-stu-id="b7040-414">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange server (in which case the Exchange server would have already processed rules on the message).</span></span>  <br/> |
|<span data-ttu-id="b7040-415">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="b7040-415">SPAMFILTER_ONSAVE</span></span>  <br/> |<span data-ttu-id="b7040-416">0x00000080</span><span class="sxs-lookup"><span data-stu-id="b7040-416">0x00000080</span></span>  <br/> |<span data-ttu-id="b7040-417">Un client peut appeler [IMAPIProp::SaveChanges](imapiprop-savechanges.md), définir l’indicateur **SPAMFILTER_ONSAVE** dans le paramètre _ulFlags_ pour activer le filtrage d’un message en cours d’enregistrement du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b7040-417">A client can call [IMAPIProp::SaveChanges](imapiprop-savechanges.md), setting the **SPAMFILTER_ONSAVE** flag in the  _ulFlags_ parameter to enable spam filtering on a message that is being saved.</span></span> <span data-ttu-id="b7040-418">Prise en charge de filtrage du courrier indésirable est disponible uniquement si le type d’adresse de messagerie de l’expéditeur est SMTP Simple Mail Transfer Protocol (), et le message est enregistré dans un magasin d’un fichier de dossiers personnels (PST).</span><span class="sxs-lookup"><span data-stu-id="b7040-418">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>  <br/> |
|<span data-ttu-id="b7040-419">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="b7040-419">STORE_ITEMPROC</span></span>  <br/> |<span data-ttu-id="b7040-420">0 x 00200000</span><span class="sxs-lookup"><span data-stu-id="b7040-420">0x00200000</span></span>  <br/> |<span data-ttu-id="b7040-421">Si cet indicateur est défini dans la [Propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) d’une banque de dossiers personnels encapsulée, il indique que lorsqu’un nouveau message arrive dans le magasin, le magasin possède des règles et filtrage du courrier indésirable traitées séparément dans le message.</span><span class="sxs-lookup"><span data-stu-id="b7040-421">If this flag is set in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) of a wrapped PST store, it indicates that when a new message arrives at the store, the store has rules and spam filtering processed on the message separately.</span></span> <span data-ttu-id="b7040-422">Le magasin appelle ensuite [IMAPISupport::Notify](imapisupport-notify.md), **fnevNewMail** dans la structure [NOTIFICATION](notification.md) qui est transmise en tant que paramètre et passe les détails du nouveau message à un client d’écoute.</span><span class="sxs-lookup"><span data-stu-id="b7040-422">The store then calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and passing the details of the new message to a listening client.</span></span> <span data-ttu-id="b7040-423">Par la suite, lorsque le client d’écoute reçoit la notification, il ne traite pas de règles dans le message.</span><span class="sxs-lookup"><span data-stu-id="b7040-423">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span>  <br/> |
|<span data-ttu-id="b7040-424">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="b7040-424">STORE_UNICODE_OK</span></span>  <br/> |<span data-ttu-id="b7040-425">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="b7040-425">0x00040000</span></span>  <br/> |<span data-ttu-id="b7040-426">Si cet indicateur est inclus dans la [Propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), elle indique que la banque prend en charge le stockage Unicode.</span><span class="sxs-lookup"><span data-stu-id="b7040-426">If this flag is included in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md), it indicates that the store supports Unicode storage.</span></span> <span data-ttu-id="b7040-427">Un client peut rechercher la présence de l’indicateur à décider s’il convient de demander ou d’enregistrer les informations de Unicode dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="b7040-427">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span>  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a><span data-ttu-id="b7040-428">Définitions pour l’archivage des éléments dans un dossier</span><span class="sxs-lookup"><span data-stu-id="b7040-428">Definitions for archiving items in a folder</span></span>

<span data-ttu-id="b7040-429">Les définitions de constantes suivantes sont des valeurs utilisées pour définir la [Propriété canonique PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="b7040-429">The following constant definitions are values used to set the [PidTagAgingGranularity Canonical Property](pidtagaginggranularity-canonical-property.md).</span></span>
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a><span data-ttu-id="b7040-430">Définitions d’affichage des objets distants</span><span class="sxs-lookup"><span data-stu-id="b7040-430">Definitions for displaying remote objects</span></span>

<span data-ttu-id="b7040-431">Les définitions de constante et la macro suivantes sont pour l’affichage des objets distants.</span><span class="sxs-lookup"><span data-stu-id="b7040-431">The following constant and macro definitions are for displaying remote objects.</span></span> <span data-ttu-id="b7040-432">Pour plus d’informations, voir la [Propriété canonique PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="b7040-432">For more information, see the [PidTagDisplayTypeEx Canonical Property](pidtagdisplaytypeex-canonical-property.md).</span></span>
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a><span data-ttu-id="b7040-433">Définitions de carnet d’adresses Exchange et Message stockent les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b7040-433">Definitions for Exchange address book and Message store error codes</span></span>

<span data-ttu-id="b7040-434">Le texte suivant contient des définitions des codes d’erreur pour le carnet d’adresses Exchange et la banque de messages, dont la fonctionnalité de reconnexion.</span><span class="sxs-lookup"><span data-stu-id="b7040-434">The following contains error code definitions for the Exchange Address Book and Message Store, which have reconnection capability.</span></span> <span data-ttu-id="b7040-435">Le dernier appel à un déconnecté (catalogue Global) peut entraîner l’erreur **MAPI_E_END_OF_SESSION** , qui doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="b7040-435">The last call to a disconnected Global Catalog (GC) may result in the **MAPI_E_END_OF_SESSION** error, which would need to be retried.</span></span> 
  
<span data-ttu-id="b7040-436">MAPI prend en charge la reconnexion d’Outlook à un serveur de catalogue global sans reconfiguration spéciale, mais d’autres erreurs codes peuvent être renvoyés au client.</span><span class="sxs-lookup"><span data-stu-id="b7040-436">Outlook's MAPI supports reconnection to a GC server without special reconfiguration, but some other error codes can be returned to the client.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="b7040-437">MAPI_E_END_OF_SESSION</span><span class="sxs-lookup"><span data-stu-id="b7040-437">MAPI_E_END_OF_SESSION</span></span>  <br/> |<span data-ttu-id="b7040-438">0x80040200</span><span class="sxs-lookup"><span data-stu-id="b7040-438">0x80040200</span></span>  <br/> |<span data-ttu-id="b7040-439">Retourné lorsqu’une connexion a été déconnectée.</span><span class="sxs-lookup"><span data-stu-id="b7040-439">Returned when a connection has been disconnected.</span></span>  <br/> |
|<span data-ttu-id="b7040-440">MAPI_E_RECONNECTED</span><span class="sxs-lookup"><span data-stu-id="b7040-440">MAPI_E_RECONNECTED</span></span>  <br/> |<span data-ttu-id="b7040-441">0 x 80040125</span><span class="sxs-lookup"><span data-stu-id="b7040-441">0x80040125</span></span>  <br/> |<span data-ttu-id="b7040-442">Renvoyé lorsque le jeton de connexion de l’appel de procédure distante (RPC) est obsolète.</span><span class="sxs-lookup"><span data-stu-id="b7040-442">Returned when the Remote Procedure Call (RPC) connection token is out-of-date.</span></span> <span data-ttu-id="b7040-443">Si le jeton de la transaction actuelle est différent du jeton de la connexion, cela signifie qu’il s’est reconnecté, afin que **MAPI_E_RECONNECTED** est retourné et peut être traitée comme **MAPI_E_END_OF_SESSION**.</span><span class="sxs-lookup"><span data-stu-id="b7040-443">If the token of the current transaction is different from the token of the connection that means it has reconnected, so **MAPI_E_RECONNECTED** is returned and can be treated the same as **MAPI_E_END_OF_SESSION**.</span></span> <span data-ttu-id="b7040-444">L’appel doit être relancée.</span><span class="sxs-lookup"><span data-stu-id="b7040-444">The call should be retried.</span></span>  <br/> |
|<span data-ttu-id="b7040-445">MAPI_E_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="b7040-445">MAPI_E_OFFLINE</span></span>  <br/> |<span data-ttu-id="b7040-446">0x80040126</span><span class="sxs-lookup"><span data-stu-id="b7040-446">0x80040126</span></span>  <br/> |<span data-ttu-id="b7040-447">Renvoyé lorsque la connexion est en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="b7040-447">Returned when the connection is offline.</span></span> <span data-ttu-id="b7040-448">En règle générale, cela signifie que quelque chose s’est produite dans l’environnement, telles que la défaillance du serveur ou de perte de connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="b7040-448">Typically this means that something has occurred in the environment, such as server failure or loss of network connectivity.</span></span> <span data-ttu-id="b7040-449">Cette erreur est susceptible de se produire lors de l’utilisation d’un mode mis en cache de profil et tente de contourner le cache pour communiquer avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="b7040-449">This error is most likely to occur when using a cached mode profile and attempting to bypass the cache to communicate with the server.</span></span> <span data-ttu-id="b7040-450">Si le cache n’a jamais pu initialement établir une connexion au serveur, il peut être à l’état en mode hors connexion dans lequel **MAPI_E_OFFLINE** pourrait exposer.</span><span class="sxs-lookup"><span data-stu-id="b7040-450">If the cache was never able to initially establish a connection to the server, it may be in the offline state in which **MAPI_E_OFFLINE** could surface.</span></span>  <br/> |
   
<span data-ttu-id="b7040-451">Aucune de ces deux erreurs s’afficheront dans tous les scénarios où ils apparaîtraient probablement à appliquer.</span><span class="sxs-lookup"><span data-stu-id="b7040-451">Neither of the preceding two errors will be returned in all scenarios where they would likely appear to apply.</span></span> <span data-ttu-id="b7040-452">Dans la plupart des cas, **MAPI\_E_NETWORK_ERROR** ou **MAPI_E_CALL_FAILED** seront retournés.</span><span class="sxs-lookup"><span data-stu-id="b7040-452">In most cases, **MAPI\_E_NETWORK_ERROR** or **MAPI_E_CALL_FAILED** will be returned.</span></span> <span data-ttu-id="b7040-453">Ne s’affiche à l’aide du téléchargement de [Microsoft Exchange Server MAPI Client et Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) .</span><span class="sxs-lookup"><span data-stu-id="b7040-453">Neither will appear using the [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) download.</span></span> 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a><span data-ttu-id="b7040-454">Définitions de boîte aux lettres du serveur Exchange mis en cache des quotas de mode</span><span class="sxs-lookup"><span data-stu-id="b7040-454">Definitions for Exchange Server Mailbox cached mode quotas</span></span>

<span data-ttu-id="b7040-455">Les définitions de constantes suivantes sont utilisées par Microsoft Outlook 2010 et Microsoft Outlook 2013 pour définir la version d’Exchange mis en cache les quotas de profils en mode qui sont équivalents aux quotas de boîte aux lettres Exchange dans le cas contraire disponibles uniquement avec un profil en ligne.</span><span class="sxs-lookup"><span data-stu-id="b7040-455">The following constant definitions are used by Microsoft Outlook 2010 and Microsoft Outlook 2013 to set the Exchange cached mode profile quotas that are equivalent to the Exchange mailbox quotas otherwise available only with an online profile.</span></span>
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

<span data-ttu-id="b7040-456">Ces propriétés correspondent aux leurs propriétés online correspondantes et contiennent les mêmes valeurs en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="b7040-456">These properties map to their correspondent online properties and contain the same values in kilobytes.</span></span> <span data-ttu-id="b7040-457">PR_QUOTA_WARNING mappe sur PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND à PR_QUOTA_PROHIBIT_SEND_QUOTA et PR_QUOTA_RECEIVE à PR_PROHIBIT_RECEIVE_QUOTA.</span><span class="sxs-lookup"><span data-stu-id="b7040-457">PR_QUOTA_WARNING maps to PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND to PR_QUOTA_PROHIBIT_SEND_QUOTA, and PR_QUOTA_RECEIVE to PR_PROHIBIT_RECEIVE_QUOTA.</span></span>
  
### <a name="definitions-for-message-format"></a><span data-ttu-id="b7040-458">Définitions de format de message</span><span class="sxs-lookup"><span data-stu-id="b7040-458">Definitions for message format</span></span>

<span data-ttu-id="b7040-459">Les définitions de constantes suivantes sont des valeurs qui sont utilisées pour définir la [Propriété canonique PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="b7040-459">The following constant definitions are values that are used to set the [PidTagMessageEditorFormat Canonical Property](pidtagmessageeditorformat-canonical-property.md).</span></span>
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a><span data-ttu-id="b7040-460">Définitions à l’aide de RPC sur HTTP</span><span class="sxs-lookup"><span data-stu-id="b7040-460">Definitions for using RPC over HTTP</span></span>

<span data-ttu-id="b7040-461">Consultez la rubrique de la [Propriété canonique PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) pour les définitions de constantes permet de définir la propriété en tant qu’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="b7040-461">See the [PidTagRpcOverHttpFlags Canonical Property](pidtagrpcoverhttpflags-canonical-property.md) topic for constant definitions used as flags to set the property.</span></span> 
  
<span data-ttu-id="b7040-462">Consultez la rubrique de la [Propriété canonique PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) pour les définitions de constantes utilisées pour définir la propriété.</span><span class="sxs-lookup"><span data-stu-id="b7040-462">See the [PidTagRpcOverHttpProxyAuthScheme Canonical Property](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) topic for constant definitions used to set the property.</span></span> 
  
### <a name="identifiers"></a><span data-ttu-id="b7040-463">Identificateurs</span><span class="sxs-lookup"><span data-stu-id="b7040-463">Identifiers</span></span>

<span data-ttu-id="b7040-464">Utiliser le `DEFINE_OLEGUID` macro définie dans le guiddef.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows pour associer les noms symboliques GUID suivants à leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="b7040-464">Use the  `DEFINE_OLEGUID` macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the following GUID symbolic names with their values.</span></span> 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

<span data-ttu-id="b7040-465">L’identificateur suivant concerne la section Capone de carnet d’adresses qui contient une propriété [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) efficacement désactive la valeur par défaut pour plusieurs boîtes aux lettres Exchange ([MultiEx](using-multiple-exchange-accounts.md)) conteneur spécifié par [SetDefaultDir](iaddrbook-setdefaultdir.md).</span><span class="sxs-lookup"><span data-stu-id="b7040-465">The following Identifier is for the Capone Profile section of an Address Book, which in support of multiple Exchange ([MultiEx](using-multiple-exchange-accounts.md)) mailboxes contains a [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property that effectively turns off the default container specified by [SetDefaultDir](iaddrbook-setdefaultdir.md).</span></span>
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a><span data-ttu-id="b7040-466">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="b7040-466">Interface identifiers</span></span>

#### <a name="imapisync"></a><span data-ttu-id="b7040-467">IMAPISync</span><span class="sxs-lookup"><span data-stu-id="b7040-467">IMAPISync</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a><span data-ttu-id="b7040-468">IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="b7040-468">IMAPISyncProgressCallback</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a><span data-ttu-id="b7040-469">IID_IContabAdmin</span><span class="sxs-lookup"><span data-stu-id="b7040-469">IID_IContabAdmin</span></span>
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a><span data-ttu-id="b7040-470">IID_IMAPISECUREMESSAGE</span><span class="sxs-lookup"><span data-stu-id="b7040-470">IID_IMAPISECUREMESSAGE</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a><span data-ttu-id="b7040-471">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="b7040-471">IID_IMAPIGetSession</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a><span data-ttu-id="b7040-472">Identificateurs d’interface Gestionnaire de remplacer des fichiers PST</span><span class="sxs-lookup"><span data-stu-id="b7040-472">PST Override Handler interface identifiers</span></span>

#### <a name="iidipstoverridereq"></a><span data-ttu-id="b7040-473">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="b7040-473">IID_IPSTOVERRIDEREQ</span></span>
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a><span data-ttu-id="b7040-474">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="b7040-474">IID_IPSTOVERRIDE1</span></span>
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a><span data-ttu-id="b7040-475">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7040-475">See also</span></span>

- [<span data-ttu-id="b7040-476">À propos des ajouts MAPI</span><span class="sxs-lookup"><span data-stu-id="b7040-476">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="b7040-477">À propos des propriétés nommées utilisées par Outlook</span><span class="sxs-lookup"><span data-stu-id="b7040-477">About Named Properties Used by Outlook</span></span>](about-named-properties-used-by-outlook.md)
- [<span data-ttu-id="b7040-478">Accès un magasin sur le Remote Server quand Outlook est en Mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="b7040-478">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="b7040-479">Ouvrir un objet Store sur le Remote Server quand Outlook est en Mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="b7040-479">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="b7040-480">Gérer un Message dans un fichier OST sans appeler une synchronisation en Mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="b7040-480">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

