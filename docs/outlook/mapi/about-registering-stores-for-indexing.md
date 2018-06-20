---
title: Sur l’inscription des magasins pour l’indexation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b16446644c360185908e7f4e58463257fe17f403
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782864"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="44d8d-103">Sur l’inscription des magasins pour l’indexation</span><span class="sxs-lookup"><span data-stu-id="44d8d-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="44d8d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44d8d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44d8d-105">Cette rubrique est spécifique à la recherche instantanée dans Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="44d8d-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="44d8d-106">Recherche instantanée vous permet de rechercher rapidement des éléments dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="44d8d-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="44d8d-107">Il utilise des composants de Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="44d8d-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="44d8d-108">Le Gestionnaire de protocole MAPI vérifie le Registre Windows pour les magasins il doit indexer à des fins de recherche.</span><span class="sxs-lookup"><span data-stu-id="44d8d-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="44d8d-109">Fournisseurs de magasins indexer doivent être enregistrés dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="44d8d-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="44d8d-110">Par défaut, Windows Desktop Search ajoute quatre types de fournisseurs de magasins suivants dans le Registre Windows pour autoriser l’indexation :</span><span class="sxs-lookup"><span data-stu-id="44d8d-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="44d8d-111">Magasin de fichiers de dossiers personnels (. (PST).</span><span class="sxs-lookup"><span data-stu-id="44d8d-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="44d8d-112">Banque d’informations Microsoft Exchange, y compris les fichiers du dossier en mode hors connexion (.ost).</span><span class="sxs-lookup"><span data-stu-id="44d8d-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="44d8d-113">Banque de dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="44d8d-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="44d8d-114">Magasin pour Microsoft Office Outlook Connector pour MSN.</span><span class="sxs-lookup"><span data-stu-id="44d8d-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="44d8d-115">Fournisseurs de magasins tiers indexer doivent s’inscrire dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="44d8d-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="44d8d-116">Les administrateurs et les utilisateurs peuvent utiliser un paramètre de stratégie de groupe pour empêcher l’indexation des éléments Outlook de Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="44d8d-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="44d8d-117">Pour plus d’informations, voir [Extension de Windows Desktop Search](http://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="44d8d-117">For more information, see [Extending Windows Desktop Search](http://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="44d8d-118">Clés de Registre</span><span class="sxs-lookup"><span data-stu-id="44d8d-118">Registry Keys</span></span>

<span data-ttu-id="44d8d-119">Sur un ordinateur, tous les fournisseurs de banque indexer doivent être enregistrés sous un seul les trois clés de Registre suivantes dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="44d8d-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="44d8d-120">Le Gestionnaire de protocole MAPI se présente sous chacune de ces clés dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="44d8d-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="44d8d-121">\Software\Policies\Microsoft\Windows\Windows Search\ [HKLM]</span><span class="sxs-lookup"><span data-stu-id="44d8d-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search\\</span></span>
    
2. <span data-ttu-id="44d8d-122">\Software\Microsoft\Windows\Windows Search\Preferences\ [HKLM]</span><span class="sxs-lookup"><span data-stu-id="44d8d-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
3. <span data-ttu-id="44d8d-123">\Software\Microsoft\Windows\Windows Search\Preferences\ [HKCU]</span><span class="sxs-lookup"><span data-stu-id="44d8d-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
 <span data-ttu-id="44d8d-124">Chaque valeur sous la clé correspond à un fournisseur de magasins qui est indexé.</span><span class="sxs-lookup"><span data-stu-id="44d8d-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="44d8d-125">Le nom de la valeur est le GUID (Globally Unique Identifier) du fournisseur de banque, qui est de type **DWORD** et a la valeur hexadécimale 0 x 00000001.</span><span class="sxs-lookup"><span data-stu-id="44d8d-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="44d8d-126">GUID pour les fournisseurs de banque d’informations</span><span class="sxs-lookup"><span data-stu-id="44d8d-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="44d8d-127">La propriété MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** Spécifie le GUID d’un magasin MAPI.</span><span class="sxs-lookup"><span data-stu-id="44d8d-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="44d8d-128">Les GUID pour les fournisseurs de magasins qu’index Outlook sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="44d8d-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="44d8d-129">**Type du fournisseur de banque**</span><span class="sxs-lookup"><span data-stu-id="44d8d-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="44d8d-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="44d8d-130">**GUID**</span></span> <br/> |<span data-ttu-id="44d8d-131">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="44d8d-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="44d8d-132">Fichiers de dossiers personnels (. PST)</span><span class="sxs-lookup"><span data-stu-id="44d8d-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="44d8d-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="44d8d-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="44d8d-134">GUID est décrit en détail la mspst.h de fichier d’en-tête public **MSPST_UID_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="44d8d-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="44d8d-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="44d8d-135">Exchange</span></span>  <br/> |<span data-ttu-id="44d8d-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="44d8d-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="44d8d-137">GUID est décrit en détail la edkmdb.h de fichier d’en-tête public **pbExchangeProviderPrimaryUserGuid**</span><span class="sxs-lookup"><span data-stu-id="44d8d-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="44d8d-138">Dossiers publics</span><span class="sxs-lookup"><span data-stu-id="44d8d-138">Public folders</span></span>  <br/> |<span data-ttu-id="44d8d-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="44d8d-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="44d8d-140">GUID est décrit en détail la edkmdb.h de fichier d’en-tête public **pbExchangeProviderPublicGuid**</span><span class="sxs-lookup"><span data-stu-id="44d8d-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="44d8d-141">Outlook Connector pour MSN</span><span class="sxs-lookup"><span data-stu-id="44d8d-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="44d8d-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="44d8d-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="44d8d-143">Aucun</span><span class="sxs-lookup"><span data-stu-id="44d8d-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44d8d-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44d8d-144">See also</span></span>



[<span data-ttu-id="44d8d-145">À propos de l’API du magasin</span><span class="sxs-lookup"><span data-stu-id="44d8d-145">About the Store API</span></span>](about-the-store-api.md)

