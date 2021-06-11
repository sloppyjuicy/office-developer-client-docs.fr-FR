---
title: À propos de l’inscription des magasins pour l’indexation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321825"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="91616-103">À propos de l’inscription des magasins pour l’indexation</span><span class="sxs-lookup"><span data-stu-id="91616-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="91616-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91616-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91616-105">Cette rubrique est spécifique à la recherche instantanée dans Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="91616-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="91616-106">La recherche instantanée vous permet de trouver rapidement des éléments dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="91616-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="91616-107">Il utilise des composants de Windows recherche de bureau.</span><span class="sxs-lookup"><span data-stu-id="91616-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="91616-108">Le handler de protocole MAPI vérifie la Windows registre pour les magasins qu’il doit indexer à des fins de recherche.</span><span class="sxs-lookup"><span data-stu-id="91616-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="91616-109">Les fournisseurs du Windows Store qui souhaitent être indexés doivent être inscrits dans Windows registre.</span><span class="sxs-lookup"><span data-stu-id="91616-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="91616-110">Par défaut, Windows recherche de bureau ajoute les quatre types de fournisseurs de magasins suivants au Registre Windows pour autoriser l’indexation :</span><span class="sxs-lookup"><span data-stu-id="91616-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="91616-111">Stocker les fichiers de dossiers personnels (. PST).</span><span class="sxs-lookup"><span data-stu-id="91616-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="91616-112">Microsoft Exchange store, y compris les fichiers de dossier hors connexion (.ost).</span><span class="sxs-lookup"><span data-stu-id="91616-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="91616-113">Stockez les dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="91616-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="91616-114">Store for Microsoft Office Outlook Connector for MSN.</span><span class="sxs-lookup"><span data-stu-id="91616-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="91616-115">Les fournisseurs de magasins tiers qui souhaitent être indexés doivent s’inscrire eux-mêmes dans Windows registre.</span><span class="sxs-lookup"><span data-stu-id="91616-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="91616-116">Les administrateurs et les utilisateurs peuvent utiliser un paramètre de stratégie de groupe pour empêcher Windows recherche de bureau d’indexer Outlook éléments.</span><span class="sxs-lookup"><span data-stu-id="91616-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="91616-117">Pour plus d’informations, [voir Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="91616-117">For more information, see [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="91616-118">Clés de Registre</span><span class="sxs-lookup"><span data-stu-id="91616-118">Registry Keys</span></span>

<span data-ttu-id="91616-119">Sur un ordinateur, tous les fournisseurs de magasins qui souhaitent être indexés doivent être enregistrés sous l’une des trois clés de Registre suivantes dans le Windows registre.</span><span class="sxs-lookup"><span data-stu-id="91616-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="91616-120">Le handler de protocole MAPI examine chacune de ces clés dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="91616-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="91616-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search</span><span class="sxs-lookup"><span data-stu-id="91616-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search</span></span>\
    
2. <span data-ttu-id="91616-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences</span><span class="sxs-lookup"><span data-stu-id="91616-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences</span></span>\
    
3. <span data-ttu-id="91616-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences</span><span class="sxs-lookup"><span data-stu-id="91616-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences</span></span>\
    
 <span data-ttu-id="91616-124">Chaque valeur sous la clé correspond à un fournisseur de magasins qui serait indexé.</span><span class="sxs-lookup"><span data-stu-id="91616-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="91616-125">Le nom de la valeur est l’identificateur global unique (GUID) du fournisseur de magasins, qui est du type **DWORD** et a la valeur hexadécimale 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="91616-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="91616-126">GUID pour les fournisseurs du Store</span><span class="sxs-lookup"><span data-stu-id="91616-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="91616-127">La propriété MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** le GUID d’un magasin MAPI.</span><span class="sxs-lookup"><span data-stu-id="91616-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="91616-128">Les GUID des fournisseurs de magasins qui Outlook index sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="91616-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="91616-129">**Type de fournisseur du Store**</span><span class="sxs-lookup"><span data-stu-id="91616-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="91616-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="91616-130">**GUID**</span></span> <br/> |<span data-ttu-id="91616-131">**Notes**</span><span class="sxs-lookup"><span data-stu-id="91616-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="91616-132">Fichiers de dossiers personnels (. PST)</span><span class="sxs-lookup"><span data-stu-id="91616-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="91616-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="91616-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="91616-134">Le GUID est documenté dans le fichier d’en-tête public mspst.h **comme MSPST_UID_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="91616-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="91616-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="91616-135">Exchange</span></span>  <br/> |<span data-ttu-id="91616-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="91616-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="91616-137">Le GUID est documenté dans le fichier d’en-tête public edkmdb.h en tant que **pbExchangeProviderPrimaryUserGuid**</span><span class="sxs-lookup"><span data-stu-id="91616-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="91616-138">Dossiers publics</span><span class="sxs-lookup"><span data-stu-id="91616-138">Public folders</span></span>  <br/> |<span data-ttu-id="91616-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="91616-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="91616-140">LE GUID est documenté dans le fichier d’en-tête public edkmdb.h en tant que **pbExchangeProviderPublicGuid**</span><span class="sxs-lookup"><span data-stu-id="91616-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="91616-141">Outlook Connecteur pour MSN</span><span class="sxs-lookup"><span data-stu-id="91616-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="91616-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="91616-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="91616-143">Aucun</span><span class="sxs-lookup"><span data-stu-id="91616-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91616-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91616-144">See also</span></span>



[<span data-ttu-id="91616-145">À propos de l’API de magasin</span><span class="sxs-lookup"><span data-stu-id="91616-145">About the Store API</span></span>](about-the-store-api.md)

