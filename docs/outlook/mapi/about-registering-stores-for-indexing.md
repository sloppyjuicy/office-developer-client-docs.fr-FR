---
title: À propos de l'enregistrement des magasins pour l'indexation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321825"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="465de-103">À propos de l'enregistrement des magasins pour l'indexation</span><span class="sxs-lookup"><span data-stu-id="465de-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="465de-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="465de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="465de-105">Cette rubrique est propre à la recherche instantanée dans Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="465de-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="465de-106">La recherche instantanée vous permet de trouver rapidement des éléments dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="465de-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="465de-107">Il utilise des composants de Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="465de-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="465de-108">Le gestionnaire de protocole MAPI vérifie si le Registre Windows contient des magasins qu'il doit indexer à des fins de recherche.</span><span class="sxs-lookup"><span data-stu-id="465de-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="465de-109">Les fournisseurs de banque qui souhaitent être indexés doivent être enregistrés dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="465de-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="465de-110">Par défaut, Windows Desktop Search ajoute les quatre types de fournisseurs de banque suivants au registre Windows pour permettre l'indexation:</span><span class="sxs-lookup"><span data-stu-id="465de-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="465de-111">Stocker les fichiers de dossiers personnels (. PST).</span><span class="sxs-lookup"><span data-stu-id="465de-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="465de-112">Banque Microsoft Exchange, y compris les fichiers de dossiers en mode hors connexion (. ost).</span><span class="sxs-lookup"><span data-stu-id="465de-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="465de-113">Stockez les dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="465de-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="465de-114">Stockez Microsoft Office Outlook Connector pour MSN.</span><span class="sxs-lookup"><span data-stu-id="465de-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="465de-115">Les fournisseurs de magasin tiers qui souhaitent être indexés doivent s'enregistrer dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="465de-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="465de-116">Les administrateurs et les utilisateurs peuvent utiliser un paramètre de stratégie de groupe pour empêcher la recherche sur le bureau Windows d'indexer les éléments Outlook.</span><span class="sxs-lookup"><span data-stu-id="465de-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="465de-117">Pour plus d'informations, consultez la rubrique [extension de Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="465de-117">For more information, see [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="465de-118">Clés de Registre</span><span class="sxs-lookup"><span data-stu-id="465de-118">Registry Keys</span></span>

<span data-ttu-id="465de-119">Sur un ordinateur, tous les fournisseurs de magasin qui souhaitent être indexés doivent être enregistrés sous une seule des trois clés de Registre suivantes dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="465de-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="465de-120">Le gestionnaire de protocole MAPI regarde sous chacune de ces clés dans l'ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="465de-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="465de-121">[HKLM] \Software\Policies\Microsoft\Windows\Windows Search \\</span><span class="sxs-lookup"><span data-stu-id="465de-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search\\</span></span>
    
2. <span data-ttu-id="465de-122">[HKLM] \Software\Microsoft\Windows\Windows Search\Preferences\\</span><span class="sxs-lookup"><span data-stu-id="465de-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
3. <span data-ttu-id="465de-123">[HKCU] \Software\Microsoft\Windows\Windows Search\Preferences\\</span><span class="sxs-lookup"><span data-stu-id="465de-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
 <span data-ttu-id="465de-124">Chaque valeur sous la clé correspond à un fournisseur de banque d'index qui sera indexé.</span><span class="sxs-lookup"><span data-stu-id="465de-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="465de-125">Le nom de la valeur est l'identificateur global unique (GUID) du fournisseur de banque, qui est de type **DWORD** et possède la valeur hexadécimale 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="465de-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="465de-126">GUID pour les fournisseurs de magasin</span><span class="sxs-lookup"><span data-stu-id="465de-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="465de-127">La propriété MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** spécifie le GUID d'un magasin MAPI.</span><span class="sxs-lookup"><span data-stu-id="465de-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="465de-128">Les GUID des fournisseurs de magasins qu'ils indexent sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="465de-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="465de-129">**Type de fournisseur de banque**</span><span class="sxs-lookup"><span data-stu-id="465de-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="465de-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="465de-130">**GUID**</span></span> <br/> |<span data-ttu-id="465de-131">**Notes**</span><span class="sxs-lookup"><span data-stu-id="465de-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="465de-132">Fichiers de dossiers personnels (. DOSSIERS</span><span class="sxs-lookup"><span data-stu-id="465de-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="465de-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="465de-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="465de-134">GUID est documenté dans le fichier d'en-tête public MSPST. h en tant que **MSPST_UID_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="465de-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="465de-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="465de-135">Exchange</span></span>  <br/> |<span data-ttu-id="465de-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="465de-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="465de-137">GUID est documenté dans le fichier d'en-tête public edkmdb. h en tant que **pbExchangeProviderPrimaryUserGuid**</span><span class="sxs-lookup"><span data-stu-id="465de-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="465de-138">Dossiers publics</span><span class="sxs-lookup"><span data-stu-id="465de-138">Public folders</span></span>  <br/> |<span data-ttu-id="465de-139">{70fab278-f7af-CD11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="465de-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="465de-140">GUID est documenté dans le fichier d'en-tête public edkmdb. h en tant que **pbExchangeProviderPublicGuid**</span><span class="sxs-lookup"><span data-stu-id="465de-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="465de-141">Outlook Connector pour MSN</span><span class="sxs-lookup"><span data-stu-id="465de-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="465de-142">{c34f5c97-eb05-bb4b-B199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="465de-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="465de-143">Aucun</span><span class="sxs-lookup"><span data-stu-id="465de-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="465de-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="465de-144">See also</span></span>



[<span data-ttu-id="465de-145">À propos de l’API de magasin</span><span class="sxs-lookup"><span data-stu-id="465de-145">About the Store API</span></span>](about-the-store-api.md)

