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
# <a name="mapi-constants"></a><span data-ttu-id="9b148-103">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9b148-103">MAPI constants</span></span>

<span data-ttu-id="9b148-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b148-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b148-105">Cette rubrique présente les définitions des constantes, les déclarations d’interface MAPI et les identificateurs de classe et d’interface utilisés par les API MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b148-105">This topic contains constant definitions, MAPI interface declarations, and class and interface identifiers used by the MAPI APIs.</span></span>
  
## <a name="class-and-interface-identifiers"></a><span data-ttu-id="9b148-106">Identificateurs de classe et d’interface</span><span class="sxs-lookup"><span data-stu-id="9b148-106">Class and interface identifiers</span></span>

<span data-ttu-id="9b148-107">Utilisez la macro DEFINE_GUID définie dans le fichier d’en-tête guiddef.h du kit de développement logiciel Windows (Kit SDK Windows) de Microsoft pour associer les noms symboliques de l’identificateur global unique (GUID) à leurs valeurs, sauf mention contraire.</span><span class="sxs-lookup"><span data-stu-id="9b148-107">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values, unless otherwise indicated.</span></span>
  
## <a name="attachment-security-conversion-api"></a><span data-ttu-id="9b148-108">API de conversion de sécurité des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="9b148-108">Attachment security conversion API</span></span>

<span data-ttu-id="9b148-109">Cette section contient les définitions des constantes et les identificateurs d’interface pour l’API de sécurité des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="9b148-109">This section contains constant definitions and interface identifiers for the Attachment Security API.</span></span>
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

<span data-ttu-id="9b148-110">Utilisez la macro MAPIMETHOD définie dans le fichier d’en-tête mapidefs.h du SDK Windows pour définir la fonction virtuelle pure **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span><span class="sxs-lookup"><span data-stu-id="9b148-110">Use the MAPIMETHOD macro defined in the Windows SDK header file mapidefs.h to define the pure virtual function **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span></span> 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

<span data-ttu-id="9b148-111">Utilisez la macro DECLARE_MAPI_INTERFACE_ définie dans le fichier d’en-tête mapidefs.h du SDK Windows pour définir le tableau de méthode virtuelle pour **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="9b148-111">Use the DECLARE_MAPI_INTERFACE_ macro defined in the Windows SDK header file mapidefs.h to define the virtual method table for **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span></span> 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a><span data-ttu-id="9b148-112">API de conversion MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="9b148-112">MAPI-MIME conversion API</span></span>

<span data-ttu-id="9b148-113">Cette section contient les définitions des constantes et les identificateurs de classe et d’interface pour l’API de conversion MAPI MIME.</span><span class="sxs-lookup"><span data-stu-id="9b148-113">This section contains constant definitions and class and interface identifiers for the MAPI-MIME Conversion API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="9b148-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="9b148-114">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b148-115">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="9b148-115">CCSF_SMTP</span></span>  <br/> |<span data-ttu-id="9b148-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="9b148-116">0x0002</span></span>  <br/> |
|<span data-ttu-id="9b148-117">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="9b148-117">CCSF_NOHEADERS</span></span>  <br/> |<span data-ttu-id="9b148-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="9b148-118">0x0004</span></span>  <br/> |
|<span data-ttu-id="9b148-119">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="9b148-119">CCSF_USE_TNEF</span></span>  <br/> | <span data-ttu-id="9b148-120">0x0010</span><span class="sxs-lookup"><span data-stu-id="9b148-120">0x0010</span></span>  <br/> |
|<span data-ttu-id="9b148-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="9b148-121">CCSF_INCLUDE_BCC</span></span>  <br/> |<span data-ttu-id="9b148-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="9b148-122">0x0020</span></span>  <br/> |
|<span data-ttu-id="9b148-123">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="9b148-123">CCSF_8BITHEADERS</span></span>  <br/> | <span data-ttu-id="9b148-124">0x0040</span><span class="sxs-lookup"><span data-stu-id="9b148-124">0x0040</span></span>  <br/> |
|<span data-ttu-id="9b148-125">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="9b148-125">CCSF_USE_RTF</span></span>  <br/> |<span data-ttu-id="9b148-126">0x0080</span><span class="sxs-lookup"><span data-stu-id="9b148-126">0x0080</span></span>  <br/> |
|<span data-ttu-id="9b148-127">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="9b148-127">CCSF_PLAIN_TEXT_ONLY</span></span>  <br/> |<span data-ttu-id="9b148-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="9b148-128">0x1000</span></span>  <br/> |
|<span data-ttu-id="9b148-129">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="9b148-129">CCSF_NO_MSGID</span></span>  <br/> |<span data-ttu-id="9b148-130">0x4000</span><span class="sxs-lookup"><span data-stu-id="9b148-130">0x4000</span></span>  <br/> |
|<span data-ttu-id="9b148-131">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="9b148-131">CCSF_GLOBAL_MESSAGE</span></span>  <br/> |<span data-ttu-id="9b148-132">0x00200000</span><span class="sxs-lookup"><span data-stu-id="9b148-132">0x00200000</span></span>  <br/> |
|<span data-ttu-id="9b148-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9b148-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="9b148-134">*Comme définie dans le fichier d’en-tête winerror.h du kit de développement logiciel Windows (Kit SDK Windows) de Microsoft*</span><span class="sxs-lookup"><span data-stu-id="9b148-134">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="9b148-135">Identificateurs de classe</span><span class="sxs-lookup"><span data-stu-id="9b148-135">Class identifiers</span></span>

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a><span data-ttu-id="9b148-136">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="9b148-136">Interface identifiers</span></span>

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a><span data-ttu-id="9b148-137">API de l’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="9b148-137">Offline State API</span></span>

<span data-ttu-id="9b148-138">Cette section contient les définitions des constantes et les identificateurs de classe et d’interface pour l’API de l’état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9b148-138">This section contains constant definitions and class and interface identifiers for the Offline State API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="9b148-139">Constantes</span><span class="sxs-lookup"><span data-stu-id="9b148-139">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b148-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9b148-140">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="9b148-141">*Comme définie dans le fichier d’en-tête winerror.h du kit de développement logiciel Windows (Kit SDK Windows) de Microsoft*</span><span class="sxs-lookup"><span data-stu-id="9b148-141">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="9b148-142">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="9b148-142">E_NOINTERFACE</span></span>  <br/> | <span data-ttu-id="9b148-143">*Comme définie dans le fichier d’en-tête winerror.h du kit de développement logiciel Windows (Kit SDK Windows)*</span><span class="sxs-lookup"><span data-stu-id="9b148-143">*As defined in the Windows (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="9b148-144">MAPIOFFLINE_ADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="9b148-144">MAPIOFFLINE_ADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="9b148-145">(ULONG)0</span><span class="sxs-lookup"><span data-stu-id="9b148-145">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="9b148-146">MAPIOFFLINE_UNADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="9b148-146">MAPIOFFLINE_UNADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="9b148-147">(ULONG)0</span><span class="sxs-lookup"><span data-stu-id="9b148-147">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="9b148-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="9b148-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span></span>  <br/> |<span data-ttu-id="9b148-149">1 </span><span class="sxs-lookup"><span data-stu-id="9b148-149">1</span></span>  <br/> |
|<span data-ttu-id="9b148-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="9b148-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="9b148-151">0x1</span><span class="sxs-lookup"><span data-stu-id="9b148-151">0x1</span></span>  <br/> |
|<span data-ttu-id="9b148-152">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="9b148-152">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="9b148-153">0x2</span><span class="sxs-lookup"><span data-stu-id="9b148-153">0x2</span></span>  <br/> |
|<span data-ttu-id="9b148-154">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="9b148-154">MAPIOFFLINE_FLAG_BLOCK</span></span>  <br/> |<span data-ttu-id="9b148-155">0x00002000</span><span class="sxs-lookup"><span data-stu-id="9b148-155">0x00002000</span></span>  <br/> |
|<span data-ttu-id="9b148-156">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="9b148-156">MAPIOFFLINE_FLAG_DEFAULT</span></span>  <br/> |<span data-ttu-id="9b148-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b148-157">0x00000000</span></span>  <br/> |
|<span data-ttu-id="9b148-158">MAPIOFFLINE_STATE_ALL</span><span class="sxs-lookup"><span data-stu-id="9b148-158">MAPIOFFLINE_STATE_ALL</span></span>  <br/> |<span data-ttu-id="9b148-159">0x003f037f</span><span class="sxs-lookup"><span data-stu-id="9b148-159">0x003f037f</span></span>  <br/> |
|<span data-ttu-id="9b148-160">**En ligne ou hors ligne**</span><span class="sxs-lookup"><span data-stu-id="9b148-160">**Online or offline**</span></span> <br/> ||
|<span data-ttu-id="9b148-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span><span class="sxs-lookup"><span data-stu-id="9b148-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span></span>  <br/> |<span data-ttu-id="9b148-162">0x00000003</span><span class="sxs-lookup"><span data-stu-id="9b148-162">0x00000003</span></span>  <br/> |
|<span data-ttu-id="9b148-163">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="9b148-163">MAPIOFFLINE_STATE_OFFLINE</span></span>  <br/> |<span data-ttu-id="9b148-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b148-164">0x00000001</span></span>  <br/> |
|<span data-ttu-id="9b148-165">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="9b148-165">MAPIOFFLINE_STATE_ONLINE</span></span>  <br/> |<span data-ttu-id="9b148-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9b148-166">0x00000002</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="9b148-167">Identificateurs de classe</span><span class="sxs-lookup"><span data-stu-id="9b148-167">Class identifiers</span></span>

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a><span data-ttu-id="9b148-168">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="9b148-168">Interface identifiers</span></span>

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

## <a name="outlook-named-properties"></a><span data-ttu-id="9b148-169">Propriétés nommées Outlook</span><span class="sxs-lookup"><span data-stu-id="9b148-169">Outlook named properties</span></span>

<span data-ttu-id="9b148-170">Cette section contient les définitions des constantes des propriétés nommées et de leurs espaces de noms et d’autres constantes connexes.</span><span class="sxs-lookup"><span data-stu-id="9b148-170">This section contains constant definitions for named properties and their namespaces, and other related constants.</span></span>
  
### <a name="definitions-for-named-properties"></a><span data-ttu-id="9b148-171">Définitions pour les propriétés nommées</span><span class="sxs-lookup"><span data-stu-id="9b148-171">Definitions for named properties</span></span>

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

### <a name="definitions-for-namespaces"></a><span data-ttu-id="9b148-172">Définitions pour les espaces de noms</span><span class="sxs-lookup"><span data-stu-id="9b148-172">Definitions for namespaces</span></span>

<span data-ttu-id="9b148-173">Les identificateurs globaux uniques (GUID) suivants représentent les espaces de noms des propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="9b148-173">The following globally unique identifiers (GUIDs) represent the namespaces of the named properties.</span></span>
  
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

<span data-ttu-id="9b148-174">Consultez la section Banque MAPI pour obtenir les définitions PSETID.</span><span class="sxs-lookup"><span data-stu-id="9b148-174">Refer to the section MAPI Store for the PSETID definitions.</span></span>
  
### <a name="other-constants"></a><span data-ttu-id="9b148-175">Autres constantes</span><span class="sxs-lookup"><span data-stu-id="9b148-175">Other constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b148-176">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="9b148-176">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="9b148-177">0xD000000</span><span class="sxs-lookup"><span data-stu-id="9b148-177">0xD000000</span></span>  <br/> |
|<span data-ttu-id="9b148-178">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="9b148-178">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="9b148-179">0x2000000</span><span class="sxs-lookup"><span data-stu-id="9b148-179">0x2000000</span></span>  <br/> |
|<span data-ttu-id="9b148-180">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="9b148-180">MNID_ID</span></span>  <br/> | <span data-ttu-id="9b148-181">*Comme définie dans le fichier d’en-tête mapidefs.h.*</span><span class="sxs-lookup"><span data-stu-id="9b148-181">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="9b148-182">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="9b148-182">MNID_STRING</span></span>  <br/> | <span data-ttu-id="9b148-183">*Comme définie dans le fichier d’en-tête mapidefs.h.*</span><span class="sxs-lookup"><span data-stu-id="9b148-183">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="9b148-184">mtgNone</span><span class="sxs-lookup"><span data-stu-id="9b148-184">mtgNone</span></span>  <br/> |<span data-ttu-id="9b148-185">0x0</span><span class="sxs-lookup"><span data-stu-id="9b148-185">0x0</span></span>  <br/> |
|<span data-ttu-id="9b148-186">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="9b148-186">mtgRequest</span></span>  <br/> |<span data-ttu-id="9b148-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b148-187">0x00000001</span></span>  <br/> |
|<span data-ttu-id="9b148-188">mtgFullUpdate</span><span class="sxs-lookup"><span data-stu-id="9b148-188">mtgFullUpdate</span></span>  <br/> |<span data-ttu-id="9b148-189">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-189">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-190">mtgInfoUpdate</span><span class="sxs-lookup"><span data-stu-id="9b148-190">mtgInfoUpdate</span></span>  <br/> |<span data-ttu-id="9b148-191">0x00020000</span><span class="sxs-lookup"><span data-stu-id="9b148-191">0x00020000</span></span>  <br/> |
|<span data-ttu-id="9b148-192">mtgOutofDate</span><span class="sxs-lookup"><span data-stu-id="9b148-192">mtgOutofDate</span></span>  <br/> |<span data-ttu-id="9b148-193">0x00080000</span><span class="sxs-lookup"><span data-stu-id="9b148-193">0x00080000</span></span>  <br/> |
|<span data-ttu-id="9b148-194">mtgDelegated</span><span class="sxs-lookup"><span data-stu-id="9b148-194">mtgDelegated</span></span>  <br/> |<span data-ttu-id="9b148-195">0x00100000</span><span class="sxs-lookup"><span data-stu-id="9b148-195">0x00100000</span></span>  <br/> |
   
## <a name="replication-api"></a><span data-ttu-id="9b148-196">API de réplication</span><span class="sxs-lookup"><span data-stu-id="9b148-196">Replication API</span></span>

<span data-ttu-id="9b148-197">Cette section présente les définitions des constantes, les déclarations d’interface MAPI et les identificateurs de classe et d’interface de l’API de réplication.</span><span class="sxs-lookup"><span data-stu-id="9b148-197">This section contains constant definitions, MAPI interface declarations, and class and interface identifiers for the Replication API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="9b148-198">Constantes</span><span class="sxs-lookup"><span data-stu-id="9b148-198">Constants</span></span>

<span data-ttu-id="9b148-199">Voici la structure d’une constante [MAPIUID](mapiuid.md) identifiant un fournisseur de services MAPI :</span><span class="sxs-lookup"><span data-stu-id="9b148-199">The following is a [MAPIUID](mapiuid.md) structure identifying a MAPI service provider:</span></span> 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|<span data-ttu-id="9b148-200">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-200">DNH_OK</span></span>  <br/> |<span data-ttu-id="9b148-201">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-201">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-202">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-202">DNT_OK</span></span>  <br/> |<span data-ttu-id="9b148-203">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-203">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-204">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="9b148-204">HSF_LOCAL</span></span>  <br/> |<span data-ttu-id="9b148-205">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9b148-205">0x00000008</span></span>  <br/> |
|<span data-ttu-id="9b148-206">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="9b148-206">HSF_COPYDESTRUCTIVE</span></span>  <br/> |<span data-ttu-id="9b148-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b148-207">0x00000010</span></span>  <br/> |
|<span data-ttu-id="9b148-208">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-208">HSF_OK</span></span>  <br/> |<span data-ttu-id="9b148-209">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-209">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-210">MDB_OST_LOGON_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9b148-210">MDB_OST_LOGON_UNICODE</span></span>  <br/> |<span data-ttu-id="9b148-211">((ULONG) 0x00000800)</span><span class="sxs-lookup"><span data-stu-id="9b148-211">((ULONG) 0x00000800)</span></span>  <br/> |
|<span data-ttu-id="9b148-212">MDB_OST_LOGON_ANSI</span><span class="sxs-lookup"><span data-stu-id="9b148-212">MDB_OST_LOGON_ANSI</span></span>  <br/> |<span data-ttu-id="9b148-213">((ULONG) 0x00001000)</span><span class="sxs-lookup"><span data-stu-id="9b148-213">((ULONG) 0x00001000)</span></span>  <br/> |
|<span data-ttu-id="9b148-214">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="9b148-214">SHOW_SOFT_DELETES</span></span>  <br/> |<span data-ttu-id="9b148-215">((ULONG) 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="9b148-215">((ULONG) 0x00000002)</span></span>  <br/> |
|<span data-ttu-id="9b148-216">SS_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="9b148-216">SS_ACTIVE</span></span>  <br/> |<span data-ttu-id="9b148-217">0</span><span class="sxs-lookup"><span data-stu-id="9b148-217">0</span></span>  <br/> |
|<span data-ttu-id="9b148-218">SS_SUSPENDED</span><span class="sxs-lookup"><span data-stu-id="9b148-218">SS_SUSPENDED</span></span>  <br/> |<span data-ttu-id="9b148-219">1 </span><span class="sxs-lookup"><span data-stu-id="9b148-219">1</span></span>  <br/> |
|<span data-ttu-id="9b148-220">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="9b148-220">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="9b148-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b148-221">0x00000001</span></span>  <br/> |
|<span data-ttu-id="9b148-222">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="9b148-222">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="9b148-223">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9b148-223">0x00000002</span></span>  <br/> |
|<span data-ttu-id="9b148-224">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="9b148-224">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="9b148-225">0x00000040</span><span class="sxs-lookup"><span data-stu-id="9b148-225">0x00000040</span></span>  <br/> |
|<span data-ttu-id="9b148-226">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="9b148-226">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="9b148-227">0x00000080</span><span class="sxs-lookup"><span data-stu-id="9b148-227">0x00000080</span></span>  <br/> |
|<span data-ttu-id="9b148-228">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="9b148-228">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="9b148-229">0x00000200</span><span class="sxs-lookup"><span data-stu-id="9b148-229">0x00000200</span></span>  <br/> |
|<span data-ttu-id="9b148-230">SYNC_BACKGROUND</span><span class="sxs-lookup"><span data-stu-id="9b148-230">SYNC_BACKGROUND</span></span>  <br/> |<span data-ttu-id="9b148-231">0x00001000</span><span class="sxs-lookup"><span data-stu-id="9b148-231">0x00001000</span></span>  <br/> |
|<span data-ttu-id="9b148-232">SYNC_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="9b148-232">SYNC_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="9b148-233">0x00020000</span><span class="sxs-lookup"><span data-stu-id="9b148-233">0x00020000</span></span>  <br/> |
|<span data-ttu-id="9b148-234">SYNC_HEADERS</span><span class="sxs-lookup"><span data-stu-id="9b148-234">SYNC_HEADERS</span></span>  <br/> |<span data-ttu-id="9b148-235">0x02000000</span><span class="sxs-lookup"><span data-stu-id="9b148-235">0x02000000</span></span>  <br/> |
|<span data-ttu-id="9b148-236">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-236">UPC_OK</span></span>  <br/> |<span data-ttu-id="9b148-237">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-237">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-238">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="9b148-238">UPD_ASSOC</span></span>  <br/> |<span data-ttu-id="9b148-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b148-239">0x00000001</span></span>  <br/> |
|<span data-ttu-id="9b148-240">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="9b148-240">UPD_MOV</span></span>  <br/> |<span data-ttu-id="9b148-241">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9b148-241">0x00000002</span></span>  <br/> |
|<span data-ttu-id="9b148-242">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-242">UPD_OK</span></span>  <br/> |<span data-ttu-id="9b148-243">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-243">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-244">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="9b148-244">UPD_MOVED</span></span>  <br/> |<span data-ttu-id="9b148-245">0x00020000</span><span class="sxs-lookup"><span data-stu-id="9b148-245">0x00020000</span></span>  <br/> |
|<span data-ttu-id="9b148-246">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="9b148-246">UPD_UPDATE</span></span>  <br/> |<span data-ttu-id="9b148-247">0x00040000</span><span class="sxs-lookup"><span data-stu-id="9b148-247">0x00040000</span></span>  <br/> |
|<span data-ttu-id="9b148-248">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="9b148-248">UPD_COMMIT</span></span>  <br/> |<span data-ttu-id="9b148-249">0x00080000</span><span class="sxs-lookup"><span data-stu-id="9b148-249">0x00080000</span></span>  <br/> |
|<span data-ttu-id="9b148-250">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="9b148-250">UPF_NEW</span></span>  <br/> |<span data-ttu-id="9b148-251">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b148-251">0x00000001</span></span>  <br/> |
|<span data-ttu-id="9b148-252">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="9b148-252">UPF_MOD_PARENT</span></span>  <br/> |<span data-ttu-id="9b148-253">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9b148-253">0x00000002</span></span>  <br/> |
|<span data-ttu-id="9b148-254">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="9b148-254">UPF_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="9b148-255">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9b148-255">0x00000004</span></span>  <br/> |
|<span data-ttu-id="9b148-256">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="9b148-256">UPF_DEL</span></span>  <br/> |<span data-ttu-id="9b148-257">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9b148-257">0x00000008</span></span>  <br/> |
|<span data-ttu-id="9b148-258">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-258">UPF_OK</span></span>  <br/> |<span data-ttu-id="9b148-259">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-259">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-260">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-260">UPH_OK</span></span>  <br/> |<span data-ttu-id="9b148-261">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-261">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-262">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="9b148-262">UPM_ASSOC</span></span>  <br/> |<span data-ttu-id="9b148-263">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b148-263">0x00000001</span></span>  <br/> |
|<span data-ttu-id="9b148-264">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="9b148-264">UPM_NEW</span></span>  <br/> |<span data-ttu-id="9b148-265">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9b148-265">0x00000002</span></span>  <br/> |
|<span data-ttu-id="9b148-266">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="9b148-266">UPM_MOV</span></span>  <br/> |<span data-ttu-id="9b148-267">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9b148-267">0x00000004</span></span>  <br/> |
|<span data-ttu-id="9b148-268">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="9b148-268">UPM_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="9b148-269">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9b148-269">0x00000008</span></span>  <br/> |
|<span data-ttu-id="9b148-270">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="9b148-270">UPM_HEADER</span></span>  <br/> |<span data-ttu-id="9b148-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b148-271">0x00000010</span></span>  <br/> |
|<span data-ttu-id="9b148-272">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-272">UPM_OK</span></span>  <br/> |<span data-ttu-id="9b148-273">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-273">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-274">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="9b148-274">UPM_MOVED</span></span>  <br/> |<span data-ttu-id="9b148-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="9b148-275">0x00020000</span></span>  <br/> |
|<span data-ttu-id="9b148-276">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="9b148-276">UPM_COMMIT</span></span>  <br/> |<span data-ttu-id="9b148-277">0x00040000</span><span class="sxs-lookup"><span data-stu-id="9b148-277">0x00040000</span></span>  <br/> |
|<span data-ttu-id="9b148-278">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="9b148-278">UPM_DELETE</span></span>  <br/> |<span data-ttu-id="9b148-279">0x00080000</span><span class="sxs-lookup"><span data-stu-id="9b148-279">0x00080000</span></span>  <br/> |
|<span data-ttu-id="9b148-280">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="9b148-280">UPM_SAVE</span></span>  <br/> |<span data-ttu-id="9b148-281">0x00100000</span><span class="sxs-lookup"><span data-stu-id="9b148-281">0x00100000</span></span>  <br/> |
|<span data-ttu-id="9b148-282">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="9b148-282">UPR_ASSOC</span></span>  <br/> |<span data-ttu-id="9b148-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b148-283">0x00000001</span></span>  <br/> |
|<span data-ttu-id="9b148-284">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="9b148-284">UPR_READ</span></span>  <br/> |<span data-ttu-id="9b148-285">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9b148-285">0x00000002</span></span>  <br/> |
|<span data-ttu-id="9b148-286">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-286">UPR_OK</span></span>  <br/> |<span data-ttu-id="9b148-287">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-287">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-288">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="9b148-288">UPR_COMMIT</span></span>  <br/> |<span data-ttu-id="9b148-289">0x00020000</span><span class="sxs-lookup"><span data-stu-id="9b148-289">0x00020000</span></span>  <br/> |
|<span data-ttu-id="9b148-290">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="9b148-290">UPS_UPLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="9b148-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b148-291">0x00000001</span></span>  <br/> |
|<span data-ttu-id="9b148-292">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="9b148-292">UPS_DNLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="9b148-293">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9b148-293">0x00000002</span></span>  <br/> |
|<span data-ttu-id="9b148-294">UPS_ONE_FOLDER</span><span class="sxs-lookup"><span data-stu-id="9b148-294">UPS_ONE_FOLDER</span></span>  <br/> |<span data-ttu-id="9b148-295">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9b148-295">0x00000004</span></span>  <br/> |
|<span data-ttu-id="9b148-296">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="9b148-296">UPS_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="9b148-297">0x00000080</span><span class="sxs-lookup"><span data-stu-id="9b148-297">0x00000080</span></span>  <br/> |
|<span data-ttu-id="9b148-298">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-298">UPS_OK</span></span>  <br/> |<span data-ttu-id="9b148-299">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-299">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-300">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-300">UPT_OK</span></span>  <br/> |<span data-ttu-id="9b148-301">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-301">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-302">UPT_PUBLIC</span><span class="sxs-lookup"><span data-stu-id="9b148-302">UPT_PUBLIC</span></span>  <br/> |<span data-ttu-id="9b148-303">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b148-303">0x00000001</span></span>  <br/> |
|<span data-ttu-id="9b148-304">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="9b148-304">UPV_ERROR</span></span>  <br/> |<span data-ttu-id="9b148-305">0x00010000</span><span class="sxs-lookup"><span data-stu-id="9b148-305">0x00010000</span></span>  <br/> |
|<span data-ttu-id="9b148-306">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="9b148-306">UPV_DIRTY</span></span>  <br/> |<span data-ttu-id="9b148-307">0x00020000</span><span class="sxs-lookup"><span data-stu-id="9b148-307">0x00020000</span></span>  <br/> |
|<span data-ttu-id="9b148-308">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="9b148-308">UPV_COMMIT</span></span>  <br/> |<span data-ttu-id="9b148-309">0x00040000</span><span class="sxs-lookup"><span data-stu-id="9b148-309">0x00040000</span></span>  <br/> |
   
### <a name="interface-declarations"></a><span data-ttu-id="9b148-310">Déclarations d’interface</span><span class="sxs-lookup"><span data-stu-id="9b148-310">Interface declarations</span></span>

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a><span data-ttu-id="9b148-311">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="9b148-311">Interface identifiers</span></span>

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

<span data-ttu-id="9b148-312">Utilisez les deux identificateurs d’interface suivants avec [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir et ignorer les fournisseurs vérifiés sur un objet de dossier et un objet du message, respectivement.</span><span class="sxs-lookup"><span data-stu-id="9b148-312">Use the two following interface identifiers with [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), or [IMsgStore::OpenEntry](imsgstore-openentry.md) to open and ignore any provider check on a folder object and a message object, respectively.</span></span> 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a><span data-ttu-id="9b148-313">Banque MAPI</span><span class="sxs-lookup"><span data-stu-id="9b148-313">MAPI store</span></span>

<span data-ttu-id="9b148-314">Cette section contient les définitions des constantes et les identificateurs d’interface utilisés par des API qui créent une interface avec une banque MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b148-314">This section contains constant definitions and interface identifiers used by APIs that interface with a MAPI store.</span></span>
  
### <a name="constants"></a><span data-ttu-id="9b148-315">Constantes</span><span class="sxs-lookup"><span data-stu-id="9b148-315">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="9b148-316">fnevIndexing</span><span class="sxs-lookup"><span data-stu-id="9b148-316">fnevIndexing</span></span>  <br/> |<span data-ttu-id="9b148-317">((ULONG) 0x00010000)</span><span class="sxs-lookup"><span data-stu-id="9b148-317">((ULONG) 0x00010000)</span></span>  <br/> |<span data-ttu-id="9b148-318">Un fournisseur de banques peut indiquer **fnevIndexing** dans le membre **ulEventType** de la structure **[NOTIFICATION](notification.md)** pour informer l’indexeur qu’un objet est prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="9b148-318">A store provider can specify **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure to notify the indexer that an object is ready for indexing.</span></span> <span data-ttu-id="9b148-319">Le membre **info** de la structure **NOTIFICATION** contient une structure **[EXTENDED_NOTIFICATION](extended_notification.md)**.</span><span class="sxs-lookup"><span data-stu-id="9b148-319">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="9b148-320">FS_NONE</span><span class="sxs-lookup"><span data-stu-id="9b148-320">FS_NONE</span></span>  <br/> |<span data-ttu-id="9b148-321">0x00</span><span class="sxs-lookup"><span data-stu-id="9b148-321">0x00</span></span>  <br/> |<span data-ttu-id="9b148-322">Un client peut appeler **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** et rechercher le masque de bits renvoyé.</span><span class="sxs-lookup"><span data-stu-id="9b148-322">A client can call **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** and check for the returned bitmask.</span></span> <span data-ttu-id="9b148-323">**FS_NONE** indique que le dossier ne prend pas en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="9b148-323">**FS_NONE** indicates that the folder does not support sharing.</span></span>  <br/> |
|<span data-ttu-id="9b148-324">FS_SUPPORTS_SHARING</span><span class="sxs-lookup"><span data-stu-id="9b148-324">FS_SUPPORTS_SHARING</span></span>  <br/> |<span data-ttu-id="9b148-325">0x01</span><span class="sxs-lookup"><span data-stu-id="9b148-325">0x01</span></span>  <br/> |<span data-ttu-id="9b148-326">Un client peut appeler **IFolderSupport::GetSupportMask** et rechercher le masque de bits renvoyé.</span><span class="sxs-lookup"><span data-stu-id="9b148-326">A client can call **IFolderSupport::GetSupportMask** and check for the returned bitmask.</span></span> <span data-ttu-id="9b148-327">**FS_SUPPORTS_SHARING** indique que le dossier prend en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="9b148-327">**FS_SUPPORTS_SHARING** indicates that the folder supports sharing.</span></span>  <br/> |
|<span data-ttu-id="9b148-328">INDEXING_SEARCH_OWNER</span><span class="sxs-lookup"><span data-stu-id="9b148-328">INDEXING_SEARCH_OWNER</span></span>  <br/> |<span data-ttu-id="9b148-329">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="9b148-329">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="9b148-330">Identifie le processus qui émet une notification à un indexeur indiquant qu’un objet est prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="9b148-330">Identifies the process that is pushing a notification to an indexer that an object is ready for indexing.</span></span>  <br/> |
|<span data-ttu-id="9b148-331">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="9b148-331">MNID_ID</span></span>  <br/> |<span data-ttu-id="9b148-332">Comme définie dans le fichier d’en-tête mapidefs.h du kit de développement logiciel Windows (Kit SDK Windows) de Microsoft</span><span class="sxs-lookup"><span data-stu-id="9b148-332">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h</span></span>  <br/> |<span data-ttu-id="9b148-333">Valeur pour le champ **ulKind** de la structure **[MAPINAMEID](mapinameid.md)**.</span><span class="sxs-lookup"><span data-stu-id="9b148-333">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="9b148-334">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="9b148-334">MNID_STRING</span></span>  <br/> |<span data-ttu-id="9b148-335">Comme définie dans le fichier d’en-tête mapidefs.h du kit de développement logiciel Windows (Kit SDK Windows) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9b148-335">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h.</span></span>  <br/> |<span data-ttu-id="9b148-336">Valeur pour le champ **ulKind** de la structure **[MAPINAMEID](mapinameid.md)**.</span><span class="sxs-lookup"><span data-stu-id="9b148-336">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="9b148-337">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="9b148-337">MSCAP_RES_ANNOTATION</span></span>  <br/> |<span data-ttu-id="9b148-338">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="9b148-338">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="9b148-339">Si un client spécifie **MSCAP_SEL_RESTRICTION** dans *mscapSelector* pour **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** peut renvoyer cette valeur si la banque ignore les paramètres non valides dans une restriction.</span><span class="sxs-lookup"><span data-stu-id="9b148-339">If a client specifies **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  for **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** can return this value if the store ignores invalid parameters in a restriction.</span></span>  <br/> |
|<span data-ttu-id="9b148-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="9b148-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>  <br/> |<span data-ttu-id="9b148-341">((ULONG) 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="9b148-341">((ULONG) 0x00000020)</span></span>  <br/> |<span data-ttu-id="9b148-342">Si un client spécifie **MSCAP_SEL_FOLDER** dans *mscapSelector* pour **IMSCapabilities::GetCapabilities**, **GetCapabilities** peut renvoyer cette valeur si la banque est une banque non définie par défaut qui prend en charge les pages d’accueil du dossier.</span><span class="sxs-lookup"><span data-stu-id="9b148-342">If a client specifies **MSCAP_SEL_FOLDER** in  *mscapSelector*  for **IMSCapabilities::GetCapabilities**, **GetCapabilities** can return this value if the store is a non-default store that supports folder home pages.</span></span>  <br/> |
|<span data-ttu-id="9b148-343">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-343">STORE_PUSHER_OK</span></span>  <br/> |<span data-ttu-id="9b148-344">((ULONG) 0x00800000)</span><span class="sxs-lookup"><span data-stu-id="9b148-344">((ULONG) 0x00800000)</span></span>  <br/> |<span data-ttu-id="9b148-345">Un client peut accéder à la propriété **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** pour déterminer la caractéristique d’une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="9b148-345">A client can get the property **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** to determine the characteristic of a message store.</span></span> <span data-ttu-id="9b148-346">Si le fournisseur de banques définit l’indicateur **STORE_PUSHER_OK** dans le masque de bits, cela signifie que le gestionnaire de protocole MAPI n’analysera pas la banque et que cette dernière est responsable de la transmission des modifications via l’envoi de notifications à l’indexeur afin d’indexer des messages.</span><span class="sxs-lookup"><span data-stu-id="9b148-346">If the store provider sets the **STORE_PUSHER_OK** flag in the bitmask, that means the MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>  <br/> |
   
### <a name="definitions-for-namespaces"></a><span data-ttu-id="9b148-347">Définitions pour les espaces de noms</span><span class="sxs-lookup"><span data-stu-id="9b148-347">Definitions for namespaces</span></span>

<span data-ttu-id="9b148-348">Les identificateurs globaux uniques (GUID) suivants représentent les espaces de noms des propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="9b148-348">The following globally unique identifiers (GUIDs) represent the namespaces of named properties.</span></span> <span data-ttu-id="9b148-349">Ils sont indexés par le gestionnaire de protocole MAPI et sont présentés en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9b148-349">They are indexed by the MAPI Protocol Handler (PH), and are documented as read-only.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="9b148-350">Les propriétés nommées ne doivent pas être utilisées pour créer ou modifier des éléments.</span><span class="sxs-lookup"><span data-stu-id="9b148-350">The named properties should not be used to create or modify items.</span></span> 
  
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

#### <a name="mnid_id-properties"></a><span data-ttu-id="9b148-351">Propriétés MNID_ID</span><span class="sxs-lookup"><span data-stu-id="9b148-351">MNID_ID Properties</span></span>
  
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

#### <a name="mnid_string-properties"></a><span data-ttu-id="9b148-352">Propriétés MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="9b148-352">MNID_STRING Properties</span></span>
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a><span data-ttu-id="9b148-353">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="9b148-353">Interface identifiers</span></span>

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

<span data-ttu-id="9b148-354">Utilisez la macro `DEFINE_OLEGUID` définie dans le fichier d’en-tête guiddef.h du SDK Windows pour associer le nom symbolique GUID suivant à sa valeur.</span><span class="sxs-lookup"><span data-stu-id="9b148-354">Use the  `DEFINE_OLEGUID` macro defined in the Windows SDK header file guiddef.h to associate the following GUID symbolic name with its value.</span></span> 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a><span data-ttu-id="9b148-355">Constantes de carnet d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="9b148-355">MAPI Address Book constants</span></span>

<span data-ttu-id="9b148-356">Cette section contient les définitions des constantes pour le carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b148-356">This section contains constant definitions for the MAPI Address Book.</span></span>
  
### <a name="constants"></a><span data-ttu-id="9b148-357">Constantes</span><span class="sxs-lookup"><span data-stu-id="9b148-357">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="9b148-358">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="9b148-358">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="9b148-359">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="9b148-359">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="9b148-360">Dossier racine d’un objet de carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b148-360">The root folder for a MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="9b148-361">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="9b148-361">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="9b148-362">((ULONG) 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="9b148-362">((ULONG) 0x00000002)</span></span>  <br/> |<span data-ttu-id="9b148-363">Sous-dossier inclus dans le dossier racine de l’objet de carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b148-363">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="9b148-364">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="9b148-364">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="9b148-365">((ULONG) 0x00000003)</span><span class="sxs-lookup"><span data-stu-id="9b148-365">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="9b148-366">Objet de conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="9b148-366">An address book container object.</span></span>  <br/> |
|<span data-ttu-id="9b148-367">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="9b148-367">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="9b148-368">((ULONG) 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="9b148-368">((ULONG) 0x00000004)</span></span>  <br/> |<span data-ttu-id="9b148-369">Objet d’utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9b148-369">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="9b148-370">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="9b148-370">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="9b148-371">((ULONG) 0x00000005)</span><span class="sxs-lookup"><span data-stu-id="9b148-371">((ULONG) 0x00000005)</span></span>  <br/> |<span data-ttu-id="9b148-372">Objet de liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="9b148-372">A distribution list object.</span></span>  <br/> |
   
## <a name="additional-mapi-constants"></a><span data-ttu-id="9b148-373">Constantes MAPI supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9b148-373">Additional MAPI constants</span></span>

<span data-ttu-id="9b148-374">Cette section contient les définitions des constantes, y compris les codes d’erreur et les identificateurs d’interface utilisés par les API MAPI non exposées et non documentées précédemment.</span><span class="sxs-lookup"><span data-stu-id="9b148-374">This section contains constant definitions including error codes, and interface identifiers used by MAPI APIs that were not previously exposed and documented.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="9b148-375">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="9b148-375">DIALOG_MODAL</span></span>  <br/> |<span data-ttu-id="9b148-376">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="9b148-376">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="9b148-377">Lorsqu’un client appelle la méthode [IAddrBook::Details](iaddrbook-details.md), le client doit définir l’indicateur **DIALOG_MODAL** dans le paramètre _ulFlags_ pour afficher la boîte de dialogue modale montrant les détails sur une entrée particulière de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="9b148-377">When a client calls the [IAddrBook::Details](iaddrbook-details.md) method, the client must set the **DIALOG_MODAL** flag in the  _ulFlags_ parameter to display the modal dialog box showing the details about a particular address book entry.</span></span> <span data-ttu-id="9b148-378">Cette constante est définie dans mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="9b148-378">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="9b148-379">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="9b148-379">ITEMPROC_FORCE</span></span>  <br/> |<span data-ttu-id="9b148-380">0x00000800</span><span class="sxs-lookup"><span data-stu-id="9b148-380">0x00000800</span></span>  <br/> |<span data-ttu-id="9b148-381">Dans Outlook 2007, les archives PST encapsulées traitent les règles et le filtrage du courrier indésirable dans les nouveaux messages avant que les clients MAPI soient avertis de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="9b148-381">In Outlook 2007, wrapped PST stores have rules and spam filtering processed on new messages before MAPI clients are notified of the new messages.</span></span> <span data-ttu-id="9b148-382">Un fournisseur ou un client utilisant la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour créer un message dans des archives PST doit définir l’indicateur **ITEMPROC_FORCE** dans le paramètre _ulFlags_ de la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour indiquer à l’archive PST que le message est éligible pour le traitement des règles avant que la banque avertisse les clients à l’écoute de l’arrivée du nouveau message.</span><span class="sxs-lookup"><span data-stu-id="9b148-382">A provider or client using the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new message in PST stores should set the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to indicate to the PST store that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="9b148-383">Notez que ce type de traitement de règles s’applique uniquement aux nouveaux messages créés sur un serveur qui n’est pas un serveur Microsoft Exchange Server, car le serveur Exchange traite les règles pour les messages contenus sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="9b148-383">Note that such rules processing only applies to new messages created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="9b148-384">Par conséquent, le fournisseur ou le client à l’origine de la création du message doit valider cet indicateur conjointement à **NON_EMS_XP_SAVE**, qui indique que le serveur n’est pas un serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="9b148-384">Hence the provider or client creating the message must pass this flag in combination with **NON_EMS_XP_SAVE**, which indicates the server is not an Exchange server.</span></span>  <br/> |
| <span data-ttu-id="9b148-385">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="9b148-385">MAPI_BG_SESSION</span></span>  <br/> |<span data-ttu-id="9b148-386">0x00200000</span><span class="sxs-lookup"><span data-stu-id="9b148-386">0x00200000</span></span>  <br/> |<span data-ttu-id="9b148-387">Un client peut appeler la fonction [MAPILogonEx](mapilogonex.md) en définissant l’indicateur **MAPI_BG_SESSION** dans le paramètre _flFlags_ pour se connecter à une session et effectuer les opérations en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="9b148-387">A client can call the [MAPILogonEx](mapilogonex.md) function, setting the **MAPI_BG_SESSION** flag in the  _flFlags_ parameter to log on to a session and carry out any operations in the background.</span></span> <span data-ttu-id="9b148-388">En règle générale, si un client souhaite effectuer un traitement sur un thread d’arrière-plan ou dans un processus distinct d'une façon qui soit compatible avec le thread de premier plan, il doit appeler [MAPILogonEx](mapilogonex.md) avec l’indicateur **MAPI_BG_SESSION**.</span><span class="sxs-lookup"><span data-stu-id="9b148-388">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call [MAPILogonEx](mapilogonex.md) with the **MAPI_BG_SESSION** flag.</span></span> <span data-ttu-id="9b148-389">Ce procédé est par exemple utilisé lorsqu’une application cliente, telle que le moteur d’indexation, ouvre un fichier de dossiers personnels (PST) pour l’accès aux types en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="9b148-389">An example where this is used is a client application, such as an indexing engine, opening a Personal Folders File (PST) for background type access.</span></span>  <br/> |
|<span data-ttu-id="9b148-390">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="9b148-390">MAPI_CACHE_ONLY</span></span>  <br/> |<span data-ttu-id="9b148-391">0x00004000</span><span class="sxs-lookup"><span data-stu-id="9b148-391">0x00004000</span></span>  <br/> |<span data-ttu-id="9b148-392">Un client peut appeler la méthode [IAddrBook::OpenEntry](iaddrbook-openentry.md) en définissant l’indicateur **MAPI_CACHE_ONLY** dans le paramètre _ulFlags_ pour ouvrir une entrée de carnet d’adresses et y accéder par la suite exclusivement à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="9b148-392">A client can call the [IAddrBook::OpenEntry](iaddrbook-openentry.md) method, setting the **MAPI_CACHE_ONLY** flag in the  _ulFlags_ parameter to open an address book entry and to access it subsequently only from the cache.</span></span> <span data-ttu-id="9b148-393">Ce procédé est par exemple utilisé dans une application cliente qui souhaite ouvrir la liste d’adresses globale en mode Exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="9b148-393">An example where this is used is a client application that wants to open the Global Address List in Cached Exchange mode and access an entry in that Address Book from the cache without creating traffic between the client and the server.</span></span>  <br/> |
|<span data-ttu-id="9b148-394">MAPI_DIALOG_MODELESS</span><span class="sxs-lookup"><span data-stu-id="9b148-394">MAPI_DIALOG_MODELESS</span></span>  <br/> |<span data-ttu-id="9b148-395">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="9b148-395">0x0000000C</span></span>  <br/> |<span data-ttu-id="9b148-396">Cette valeur peut être transmise à la fonction MAPISendMail Simple MAPI dans le paramètre _ulFlags_ pour spécifier qu’une boîte de dialogue non modale est affichée par l’application de courrier par défaut.</span><span class="sxs-lookup"><span data-stu-id="9b148-396">This value can be passed to the Simple MAPI MAPISendMail function in the  _ulFlags_ parameter to specify that a modeless dialog box is displayed by the default mail application.</span></span> <span data-ttu-id="9b148-397">Si ni cet indicateur, ni MAPI_DIALOG (0x00000008) ne sont définis, aucune boîte de dialogue ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9b148-397">If neither this flag nor MAPI_DIALOG (0x00000008) is set, no dialog box is displayed.</span></span>  <br/> |
|<span data-ttu-id="9b148-398">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="9b148-398">MAPI_NO_CACHE</span></span>  <br/> |<span data-ttu-id="9b148-399">0x00000200</span><span class="sxs-lookup"><span data-stu-id="9b148-399">0x00000200</span></span>  <br/> |<span data-ttu-id="9b148-400">Si Microsoft Office Outlook est en mode Exchange mis en cache et qu’une banque a été ouverte en mode mis en cache, le client ou le fournisseur de services peut appeler [IMsgStore::OpenEntry](imsgstore-openentry.md) en définissant l’indicateur **MAPI_NO_CACHE** dans le paramètre _ulFlags_ pour ouvrir un élément ou un dossier dans la banque à distance.</span><span class="sxs-lookup"><span data-stu-id="9b148-400">If Microsoft Office Outlook is in Cached Exchange Mode and a store has been opened in cached mode, a client or service provider can call [IMsgStore::OpenEntry](imsgstore-openentry.md), setting the **MAPI_NO_CACHE** flag in the  _ulFlags_ parameter to open an item or a folder on the remote store.</span></span> <span data-ttu-id="9b148-401">Notez que si vous ouvrez la banque de messages avec l’indicateur **MDB_ONLINE** sur le serveur distant, vous n’êtes pas obligé d’utiliser l’indicateur **MAPI_NO_CACHE**.</span><span class="sxs-lookup"><span data-stu-id="9b148-401">Note that if you open the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span>  <br/> |
|<span data-ttu-id="9b148-402">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9b148-402">MAPI_UNICODE</span></span>  <br/> |<span data-ttu-id="9b148-403">0x80000000</span><span class="sxs-lookup"><span data-stu-id="9b148-403">0x80000000</span></span>  <br/> |<span data-ttu-id="9b148-404">Un client ou un fournisseur de services peut appeler la fonction [OpenIMsgOnIStg](openimsgonistg.md) en définissant l’indicateur **MAPI_UNICODE** dans le paramètre _ulFlags_ pour créer des fichiers .msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="9b148-404">A client or service provider can call the [OpenIMsgOnIStg](openimsgonistg.md) function, setting the **MAPI_UNICODE** flag in the  _ulFlags_ parameter to create Unicode .msg files.</span></span> <span data-ttu-id="9b148-405">Le fichier [IMessage : IMAPIProp](imessageimapiprop.md) obtenu indique **STORE_UNICODE_OK** dans sa [propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) et prend en charge les propriétés Unicode.</span><span class="sxs-lookup"><span data-stu-id="9b148-405">The resulting [IMessage : IMAPIProp](imessageimapiprop.md) file shows **STORE_UNICODE_OK** in its [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> <span data-ttu-id="9b148-406">Cette constante est définie dans mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="9b148-406">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="9b148-407">MDB_ONLINE</span><span class="sxs-lookup"><span data-stu-id="9b148-407">MDB_ONLINE</span></span>  <br/> |<span data-ttu-id="9b148-408">0x00000100</span><span class="sxs-lookup"><span data-stu-id="9b148-408">0x00000100</span></span>  <br/> |<span data-ttu-id="9b148-409">Si Outlook est en mode Exchange mis en cache, le client ou le fournisseur de services peut appeler la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) en définissant l’indicateur **MDB_ONLINE** dans le paramètre _ulFlags_ pour remplacer la connexion à la banque de messages locale et ouvrir la banque sur le serveur distant.</span><span class="sxs-lookup"><span data-stu-id="9b148-409">If Outlook is in Cached Exchange Mode, a client or service provider can call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method, setting the **MDB_ONLINE** flag in the  _ulFlags_ parameter to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="9b148-410">Notez que vous ne pouvez pas ouvrir une banque d'informations Exchange en mode mis en cache et en mode non mis en cache simultanément dans la même session MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b148-410">Note that you cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="9b148-411">Si vous avez déjà ouvert la banque de messages mise en cache, vous devez fermer la banque avant de l’ouvrir avec cet indicateur, ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d'informations Exchange sur le serveur distant à l’aide de cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="9b148-411">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>  <br/> |
|<span data-ttu-id="9b148-412">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="9b148-412">NON_EMS_XP_SAVE</span></span>  <br/> |<span data-ttu-id="9b148-413">0x00001000</span><span class="sxs-lookup"><span data-stu-id="9b148-413">0x00001000</span></span>  <br/> |<span data-ttu-id="9b148-414">Un client peut appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en définissant l’indicateur **NON_EMS_XP_SAVE** dans le paramètre _ulFlags_ pour indiquer que le message n’a pas été remis à partir d’un serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="9b148-414">A client can call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method, setting the **NON_EMS_XP_SAVE** flag in the  _ulFlags_ parameter to indicate that the message has not been delivered from an Exchange server.</span></span> <span data-ttu-id="9b148-415">Cet indicateur doit être utilisé conjointement avec l’indicateur **ITEMPROC_FORCE** dans le paramètre _ulFlags_ pour indiquer à l’archive PST que le message est éligible pour le traitement des règles avant que la banque avertisse les clients à l’écoute de l’arrivée du nouveau message.</span><span class="sxs-lookup"><span data-stu-id="9b148-415">This flag should be used in combination with the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter to indicate to a PST store that the message is eligible for rules processing before the PST store notifies any listening client of the arrival of the message.</span></span> <span data-ttu-id="9b148-416">Ce traitement de règle s’applique uniquement aux nouveaux messages créés avec [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) sur un serveur qui n’est pas un serveur Exchange (en pareil cas, le serveur Exchange aurait déjà traité les règles dans le message).</span><span class="sxs-lookup"><span data-stu-id="9b148-416">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange server (in which case the Exchange server would have already processed rules on the message).</span></span>  <br/> |
|<span data-ttu-id="9b148-417">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="9b148-417">SPAMFILTER_ONSAVE</span></span>  <br/> |<span data-ttu-id="9b148-418">0x00000080</span><span class="sxs-lookup"><span data-stu-id="9b148-418">0x00000080</span></span>  <br/> |<span data-ttu-id="9b148-419">Un client peut appeler [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en définissant l’indicateur **SPAMFILTER_ONSAVE** dans le paramètre _ulFlags_ pour activer le filtrage du courrier indésirable dans un message en cours d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9b148-419">A client can call [IMAPIProp::SaveChanges](imapiprop-savechanges.md), setting the **SPAMFILTER_ONSAVE** flag in the  _ulFlags_ parameter to enable spam filtering on a message that is being saved.</span></span> <span data-ttu-id="9b148-420">La prise en charge du filtrage du courrier indésirable n’est disponible que si le type d’adresse e-mail de l’expéditeur suit le protocole SMTP et que le message est enregistré dans une banque pour un fichier de dossiers personnels (PST).</span><span class="sxs-lookup"><span data-stu-id="9b148-420">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>  <br/> |
|<span data-ttu-id="9b148-421">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="9b148-421">STORE_ITEMPROC</span></span>  <br/> |<span data-ttu-id="9b148-422">0x00200000</span><span class="sxs-lookup"><span data-stu-id="9b148-422">0x00200000</span></span>  <br/> |<span data-ttu-id="9b148-423">Si cet indicateur est défini dans la [propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) d’une archive PST encapsulée, il indique que lorsqu’un nouveau message arrive dans la banque, cette dernière traite des règles et effectue le filtrage du courrier indésirable séparément dans le message.</span><span class="sxs-lookup"><span data-stu-id="9b148-423">If this flag is set in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) of a wrapped PST store, it indicates that when a new message arrives at the store, the store has rules and spam filtering processed on the message separately.</span></span> <span data-ttu-id="9b148-424">La banque appelle ensuite [IMAPISupport::Notify](imapisupport-notify.md), en définissant **fnevNewMail** dans la structure [NOTIFICATION](notification.md) transmise comme paramètre et en envoyant les détails du nouveau message à un client à l’écoute.</span><span class="sxs-lookup"><span data-stu-id="9b148-424">The store then calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and passing the details of the new message to a listening client.</span></span> <span data-ttu-id="9b148-425">Par la suite, lorsque le client à l’écoute reçoit la notification, il ne traite pas de règles dans le message.</span><span class="sxs-lookup"><span data-stu-id="9b148-425">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span>  <br/> |
|<span data-ttu-id="9b148-426">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="9b148-426">STORE_UNICODE_OK</span></span>  <br/> |<span data-ttu-id="9b148-427">0x00040000</span><span class="sxs-lookup"><span data-stu-id="9b148-427">0x00040000</span></span>  <br/> |<span data-ttu-id="9b148-428">Si cet indicateur est inclus dans la [propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), il indique que la banque prend en charge le stockage Unicode.</span><span class="sxs-lookup"><span data-stu-id="9b148-428">If this flag is included in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md), it indicates that the store supports Unicode storage.</span></span> <span data-ttu-id="9b148-429">Un client peut rechercher la présence de l’indicateur pour décider s’il doit demander des informations Unicode à la banque ou les y enregistrer.</span><span class="sxs-lookup"><span data-stu-id="9b148-429">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span>  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a><span data-ttu-id="9b148-430">Définitions pour l’archivage d’éléments dans un dossier</span><span class="sxs-lookup"><span data-stu-id="9b148-430">Definitions for archiving items in a folder</span></span>

<span data-ttu-id="9b148-431">Les définitions des constantes suivantes sont des valeurs utilisées pour configurer la [propriété canonique PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="9b148-431">The following constant definitions are values used to set the [PidTagAgingGranularity Canonical Property](pidtagaginggranularity-canonical-property.md).</span></span>
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a><span data-ttu-id="9b148-432">Définitions pour l’affichage des objets distants</span><span class="sxs-lookup"><span data-stu-id="9b148-432">Definitions for displaying remote objects</span></span>

<span data-ttu-id="9b148-433">Les définitions des constantes et de macros suivantes s’appliquent à des objets distants.</span><span class="sxs-lookup"><span data-stu-id="9b148-433">The following constant and macro definitions are for displaying remote objects.</span></span> <span data-ttu-id="9b148-434">Pour obtenir plus d’informations, consultez la [propriété canonique PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="9b148-434">For more information, see the [PidTagDisplayTypeEx Canonical Property](pidtagdisplaytypeex-canonical-property.md).</span></span>
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a><span data-ttu-id="9b148-435">Définitions pour le carnet d’adresses Exchange et les codes d’erreur de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="9b148-435">Definitions for Exchange address book and Message store error codes</span></span>

<span data-ttu-id="9b148-436">Les informations suivantes contiennent des définitions de code d’erreur pour le carnet d’adresses Exchange et la banque de messages, lesquels disposent d’une fonctionnalité de reconnexion.</span><span class="sxs-lookup"><span data-stu-id="9b148-436">The following contains error code definitions for the Exchange Address Book and Message Store, which have reconnection capability.</span></span> <span data-ttu-id="9b148-437">Le dernier appel à un catalogue global déconnecté peut entraîner l’erreur **MAPI_E_END_OF_SESSION**. L’appel doit alors être retenté.</span><span class="sxs-lookup"><span data-stu-id="9b148-437">The last call to a disconnected Global Catalog (GC) may result in the **MAPI_E_END_OF_SESSION** error, which would need to be retried.</span></span> 
  
<span data-ttu-id="9b148-438">MAPI d’Outlook prend en charge la reconnexion à un serveur de catalogue global sans reconfiguration spéciale, mais certains autres codes d’erreur peuvent être renvoyés au client.</span><span class="sxs-lookup"><span data-stu-id="9b148-438">Outlook's MAPI supports reconnection to a GC server without special reconfiguration, but some other error codes can be returned to the client.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="9b148-439">MAPI_E_END_OF_SESSION</span><span class="sxs-lookup"><span data-stu-id="9b148-439">MAPI_E_END_OF_SESSION</span></span>  <br/> |<span data-ttu-id="9b148-440">0x80040200</span><span class="sxs-lookup"><span data-stu-id="9b148-440">0x80040200</span></span>  <br/> |<span data-ttu-id="9b148-441">Renvoyé si une connexion a été déconnectée.</span><span class="sxs-lookup"><span data-stu-id="9b148-441">Returned when a connection has been disconnected.</span></span>  <br/> |
|<span data-ttu-id="9b148-442">MAPI_E_RECONNECTED</span><span class="sxs-lookup"><span data-stu-id="9b148-442">MAPI_E_RECONNECTED</span></span>  <br/> |<span data-ttu-id="9b148-443">0x80040125</span><span class="sxs-lookup"><span data-stu-id="9b148-443">0x80040125</span></span>  <br/> |<span data-ttu-id="9b148-444">Renvoyé lorsque le jeton de connexion d’appel de procédure distante (RPC) est obsolète.</span><span class="sxs-lookup"><span data-stu-id="9b148-444">Returned when the Remote Procedure Call (RPC) connection token is out-of-date.</span></span> <span data-ttu-id="9b148-445">Si le jeton de la transaction actuelle est différent du jeton de la connexion, cela signifie qu’il s’est reconnecté, par conséquent **MAPI_E_RECONNECTED** est renvoyé et peut être traité de la même façon que **MAPI_E_END_OF_SESSION**.</span><span class="sxs-lookup"><span data-stu-id="9b148-445">If the token of the current transaction is different from the token of the connection that means it has reconnected, so **MAPI_E_RECONNECTED** is returned and can be treated the same as **MAPI_E_END_OF_SESSION**.</span></span> <span data-ttu-id="9b148-446">L’appel doit être retenté.</span><span class="sxs-lookup"><span data-stu-id="9b148-446">The call should be retried.</span></span>  <br/> |
|<span data-ttu-id="9b148-447">MAPI_E_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="9b148-447">MAPI_E_OFFLINE</span></span>  <br/> |<span data-ttu-id="9b148-448">0x80040126</span><span class="sxs-lookup"><span data-stu-id="9b148-448">0x80040126</span></span>  <br/> |<span data-ttu-id="9b148-449">Renvoyé lorsque la connexion est en mode hors ligne.</span><span class="sxs-lookup"><span data-stu-id="9b148-449">Returned when the connection is offline.</span></span> <span data-ttu-id="9b148-450">En règle générale, cela signifie que quelque chose s’est produit dans l’environnement, par exemple une défaillance du serveur ou une perte de connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="9b148-450">Typically this means that something has occurred in the environment, such as server failure or loss of network connectivity.</span></span> <span data-ttu-id="9b148-451">Cette erreur risque surtout de se produire lorsque vous utilisez un profil en mode mis en cache et tentez de contourner le cache pour communiquer avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="9b148-451">This error is most likely to occur when using a cached mode profile and attempting to bypass the cache to communicate with the server.</span></span> <span data-ttu-id="9b148-452">Si le cache n’a jamais réussi à établir en premier lieu une connexion au serveur, il est peut-être dans un état hors connexion où l’erreur **MAPI_E_OFFLINE** peut survenir.</span><span class="sxs-lookup"><span data-stu-id="9b148-452">If the cache was never able to initially establish a connection to the server, it may be in the offline state in which **MAPI_E_OFFLINE** could surface.</span></span>  <br/> |
   
<span data-ttu-id="9b148-453">Aucune des deux erreurs précédentes n’est renvoyée dans tous les scénarios où elles semblent s’appliquer.</span><span class="sxs-lookup"><span data-stu-id="9b148-453">Neither of the preceding two errors will be returned in all scenarios where they would likely appear to apply.</span></span> <span data-ttu-id="9b148-454">Dans la plupart des cas, **MAPI\_E_NETWORK_ERROR** ou **MAPI_E_CALL_FAILED** sera renvoyée.</span><span class="sxs-lookup"><span data-stu-id="9b148-454">In most cases, **MAPI\_E_NETWORK_ERROR** or **MAPI_E_CALL_FAILED** will be returned.</span></span> <span data-ttu-id="9b148-455">Aucune ne s’affiche si le téléchargement [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="9b148-455">Neither will appear using the [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440) download.</span></span> 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a><span data-ttu-id="9b148-456">Définitions des quotas de mode mis en cache de la boîte aux lettres du serveur Exchange</span><span class="sxs-lookup"><span data-stu-id="9b148-456">Definitions for Exchange Server Mailbox cached mode quotas</span></span>

<span data-ttu-id="9b148-457">Les définitions des constantes suivantes sont utilisées par Microsoft Outlook 2010 et Microsoft Outlook 2013 pour définir des quotas de profil du mode mis en cache Exchange équivalents aux quotas de boîte aux lettres Exchange à défaut de n’être disponibles qu’avec un profil en ligne.</span><span class="sxs-lookup"><span data-stu-id="9b148-457">The following constant definitions are used by Microsoft Outlook 2010 and Microsoft Outlook 2013 to set the Exchange cached mode profile quotas that are equivalent to the Exchange mailbox quotas otherwise available only with an online profile.</span></span>
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

<span data-ttu-id="9b148-458">Ces propriétés sont associées à leurs propriétés en ligne correspondantes et contiennent les mêmes valeurs en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="9b148-458">These properties map to their correspondent online properties and contain the same values in kilobytes.</span></span> <span data-ttu-id="9b148-459">PR_QUOTA_WARNING est associé à PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND à PR_QUOTA_PROHIBIT_SEND_QUOTA et PR_QUOTA_RECEIVE à PR_PROHIBIT_RECEIVE_QUOTA.</span><span class="sxs-lookup"><span data-stu-id="9b148-459">PR_QUOTA_WARNING maps to PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND to PR_QUOTA_PROHIBIT_SEND_QUOTA, and PR_QUOTA_RECEIVE to PR_PROHIBIT_RECEIVE_QUOTA.</span></span>
  
### <a name="definitions-for-message-format"></a><span data-ttu-id="9b148-460">Définitions du format des messages</span><span class="sxs-lookup"><span data-stu-id="9b148-460">Definitions for message format</span></span>

<span data-ttu-id="9b148-461">Les définitions des constantes suivantes sont des valeurs utilisées pour configurer la [propriété canonique PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="9b148-461">The following constant definitions are values that are used to set the [PidTagMessageEditorFormat Canonical Property](pidtagmessageeditorformat-canonical-property.md).</span></span>
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a><span data-ttu-id="9b148-462">Définitions pour utiliser RPC sur HTTP</span><span class="sxs-lookup"><span data-stu-id="9b148-462">Definitions for using RPC over HTTP</span></span>

<span data-ttu-id="9b148-463">Consultez la rubrique [Propriété canonique PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) pour obtenir les définitions des constantes utilisées comme des indicateurs pour définir la propriété.</span><span class="sxs-lookup"><span data-stu-id="9b148-463">See the [PidTagRpcOverHttpFlags Canonical Property](pidtagrpcoverhttpflags-canonical-property.md) topic for constant definitions used as flags to set the property.</span></span> 
  
<span data-ttu-id="9b148-464">Consultez la rubrique [Propriété canonique PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) pour obtenir les définitions des constantes utilisées pour définir la propriété.</span><span class="sxs-lookup"><span data-stu-id="9b148-464">See the [PidTagRpcOverHttpProxyAuthScheme Canonical Property](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) topic for constant definitions used to set the property.</span></span> 
  
### <a name="identifiers"></a><span data-ttu-id="9b148-465">Identificateurs</span><span class="sxs-lookup"><span data-stu-id="9b148-465">Identifiers</span></span>

<span data-ttu-id="9b148-466">Utilisez la macro `DEFINE_OLEGUID` définie dans le fichier d’en-tête guiddef.h du kit de développement logiciel Windows (Kit SDK Windows) de Microsoft pour associer les noms symboliques (GUID) suivants à leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="9b148-466">Use the  `DEFINE_OLEGUID` macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the following GUID symbolic names with their values.</span></span> 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

<span data-ttu-id="9b148-467">L’identificateur suivant concerne la section du profil Capone d’un carnet d’adresses qui, dans le cadre de la prise en charge de plusieurs boîtes aux lettres Exchange ([MultiEx](using-multiple-exchange-accounts.md)), contient la propriété [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) permettant de désactiver efficacement le conteneur par défaut spécifié par [SetDefaultDir](iaddrbook-setdefaultdir.md).</span><span class="sxs-lookup"><span data-stu-id="9b148-467">The following Identifier is for the Capone Profile section of an Address Book, which in support of multiple Exchange ([MultiEx](using-multiple-exchange-accounts.md)) mailboxes contains a [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property that effectively turns off the default container specified by [SetDefaultDir](iaddrbook-setdefaultdir.md).</span></span>
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a><span data-ttu-id="9b148-468">Identificateurs d’interface</span><span class="sxs-lookup"><span data-stu-id="9b148-468">Interface identifiers</span></span>

#### <a name="imapisync"></a><span data-ttu-id="9b148-469">IMAPISync</span><span class="sxs-lookup"><span data-stu-id="9b148-469">IMAPISync</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a><span data-ttu-id="9b148-470">IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="9b148-470">IMAPISyncProgressCallback</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iid_icontabadmin"></a><span data-ttu-id="9b148-471">IID_IContabAdmin</span><span class="sxs-lookup"><span data-stu-id="9b148-471">IID_IContabAdmin</span></span>
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iid_imapisecuremessage"></a><span data-ttu-id="9b148-472">IID_IMAPISECUREMESSAGE</span><span class="sxs-lookup"><span data-stu-id="9b148-472">IID_IMAPISECUREMESSAGE</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iid_imapigetsession"></a><span data-ttu-id="9b148-473">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="9b148-473">IID_IMAPIGetSession</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a><span data-ttu-id="9b148-474">Identificateurs d’interface de remplacement du gestionnaire PST</span><span class="sxs-lookup"><span data-stu-id="9b148-474">PST Override Handler interface identifiers</span></span>

#### <a name="iid_ipstoverridereq"></a><span data-ttu-id="9b148-475">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="9b148-475">IID_IPSTOVERRIDEREQ</span></span>
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iid_ipstoverride1"></a><span data-ttu-id="9b148-476">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="9b148-476">IID_IPSTOVERRIDE1</span></span>
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a><span data-ttu-id="9b148-477">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b148-477">See also</span></span>

- [<span data-ttu-id="9b148-478">À propos des ajouts MAPI</span><span class="sxs-lookup"><span data-stu-id="9b148-478">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="9b148-479">À propos des propriétés nommées utilisées par Outlook</span><span class="sxs-lookup"><span data-stu-id="9b148-479">About Named Properties Used by Outlook</span></span>](about-named-properties-used-by-outlook.md)
- [<span data-ttu-id="9b148-480">Accès à une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="9b148-480">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="9b148-481">Ouvrir une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="9b148-481">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="9b148-482">Gérer un message dans un fichier OST sans appeler de synchronisation en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="9b148-482">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

