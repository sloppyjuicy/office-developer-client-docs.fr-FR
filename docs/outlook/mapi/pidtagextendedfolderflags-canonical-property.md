---
title: Propriété canonique PidTagExtendedFolderFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 23c43586157806c603ad7fd8c146270a9d71170a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563785"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a><span data-ttu-id="673b6-103">Propriété canonique PidTagExtendedFolderFlags</span><span class="sxs-lookup"><span data-stu-id="673b6-103">PidTagExtendedFolderFlags Canonical Property</span></span>
 
<span data-ttu-id="673b6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="673b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="673b6-105">Contient des indicateurs étendues sur un dossier.</span><span class="sxs-lookup"><span data-stu-id="673b6-105">Contains extended flags about a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="673b6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="673b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="673b6-107">PR_EXTENDED_FOLDER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="673b6-107">PR_EXTENDED_FOLDER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="673b6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="673b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="673b6-109">0x36DA</span><span class="sxs-lookup"><span data-stu-id="673b6-109">0x36DA</span></span>  <br/> |
|<span data-ttu-id="673b6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="673b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="673b6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="673b6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="673b6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="673b6-112">Area:</span></span>  <br/> |<span data-ttu-id="673b6-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="673b6-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="673b6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="673b6-114">Remarks</span></span>

<span data-ttu-id="673b6-115">Cette propriété est un flux binaire qui contient des propriétés de sous-sites codées pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="673b6-115">This property is a binary stream that contains encoded sub-properties for the folder.</span></span> <span data-ttu-id="673b6-116">Il est mis en forme comme une série d’articles sub de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="673b6-116">It is formatted as a series of variable length sub items.</span></span> <span data-ttu-id="673b6-117">Les premiers 8 bits de l’élément sub est un champ ID, qui indique le type d’indicateur de l’élément sub représente.</span><span class="sxs-lookup"><span data-stu-id="673b6-117">The first 8 bits of the sub item is an ID field, which indicates what kind of flag the sub item represents.</span></span> <span data-ttu-id="673b6-118">Les deuxième 8 bits est le nombre d’octets de données qui suivent.</span><span class="sxs-lookup"><span data-stu-id="673b6-118">The second 8 bits is the number of bytes of data that follow.</span></span>
  
<span data-ttu-id="673b6-119">Valeurs d’ID possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="673b6-119">Possible ID values include:</span></span>
  
- <span data-ttu-id="673b6-120">Non valide</span><span class="sxs-lookup"><span data-stu-id="673b6-120">Invalid</span></span>
    
   <span data-ttu-id="673b6-121">N’utilisez pas cette valeur.</span><span class="sxs-lookup"><span data-stu-id="673b6-121">Do not use this value</span></span>
    
- <span data-ttu-id="673b6-122">ExtendedFlags</span><span class="sxs-lookup"><span data-stu-id="673b6-122">ExtendedFlags</span></span>
    
   <span data-ttu-id="673b6-123">Les données sont une valeur de quatre octets au format :</span><span class="sxs-lookup"><span data-stu-id="673b6-123">The data is a four byte value formatted as:</span></span>
    
   |<span data-ttu-id="673b6-124">**Bits**</span><span class="sxs-lookup"><span data-stu-id="673b6-124">**Bits**</span></span>|<span data-ttu-id="673b6-125">**Description**</span><span class="sxs-lookup"><span data-stu-id="673b6-125">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="673b6-126">0-1</span><span class="sxs-lookup"><span data-stu-id="673b6-126">0-1</span></span>  <br/> |<span data-ttu-id="673b6-127">Réservé.</span><span class="sxs-lookup"><span data-stu-id="673b6-127">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="673b6-128">2</span><span class="sxs-lookup"><span data-stu-id="673b6-128">2</span></span>  <br/> |<span data-ttu-id="673b6-129">La valeur 0 si l’application doit afficher une description de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="673b6-129">Set to 0 if the application should show a policy description.</span></span>  <br/> |
   |<span data-ttu-id="673b6-130">3-5</span><span class="sxs-lookup"><span data-stu-id="673b6-130">3-5</span></span>  <br/> |<span data-ttu-id="673b6-131">Réservé.</span><span class="sxs-lookup"><span data-stu-id="673b6-131">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="673b6-132">6 et 7</span><span class="sxs-lookup"><span data-stu-id="673b6-132">6-7</span></span>  <br/> |<span data-ttu-id="673b6-133">Contrôle l’affichage du nombre de messages dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="673b6-133">Controls the display of the number of messages in the folder.</span></span>  <br/> <span data-ttu-id="673b6-134">0 - utilisez le paramètre par défaut</span><span class="sxs-lookup"><span data-stu-id="673b6-134">0 - Use the default setting</span></span>  <br/> <span data-ttu-id="673b6-135">1 - utiliser le nombre de messages non lus</span><span class="sxs-lookup"><span data-stu-id="673b6-135">1 - Use the number of unread messages</span></span>  <br/> <span data-ttu-id="673b6-136">3 - Utilisez le nombre total de messages</span><span class="sxs-lookup"><span data-stu-id="673b6-136">3 - Use the total number of messages</span></span>  <br/> |
   |<span data-ttu-id="673b6-137">8-31</span><span class="sxs-lookup"><span data-stu-id="673b6-137">8-31</span></span>  <br/> |<span data-ttu-id="673b6-138">Réservé.</span><span class="sxs-lookup"><span data-stu-id="673b6-138">Reserved.</span></span>  <br/> |
   
<span data-ttu-id="673b6-139">Articles réservés peuvent être ignorés, mais les valeurs existantes doivent être conservés.</span><span class="sxs-lookup"><span data-stu-id="673b6-139">Reserved items can be ignored, but existing values must be preserved.</span></span>
    
- <span data-ttu-id="673b6-140">SearchFolderID</span><span class="sxs-lookup"><span data-stu-id="673b6-140">SearchFolderID</span></span>
    
   <span data-ttu-id="673b6-141">Le champ de données est un champ de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="673b6-141">The data field is a 16-byte field.</span></span> <span data-ttu-id="673b6-142">Lorsque l’application crée un dossier de recherche persistant, elle doit définir ce champ sur le dossier à la même valeur que la **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) une propriété binaire sur le Message de dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="673b6-142">When the application creates a persistent search folder, it must set this field on the folder to the same value as the **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binary property on the Search Folder Message.</span></span>
    
- <span data-ttu-id="673b6-143">ToDoFolderVersion</span><span class="sxs-lookup"><span data-stu-id="673b6-143">ToDoFolderVersion</span></span>
    
   <span data-ttu-id="673b6-144">Le champ de données est un champ de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="673b6-144">The data field is a 4-byte field.</span></span> <span data-ttu-id="673b6-145">Lorsque l’application crée le dossier de recherche des tâches, il doit définir la valeur de ce champ dans le dossier à la valeur d’entier primauté de « 0x000c0000 » :</span><span class="sxs-lookup"><span data-stu-id="673b6-145">When the application creates the to-do search folder, it must set the value of this field on the folder to the little-endian integer value of" 0x000c0000":</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="673b6-146">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="673b6-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="673b6-147">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="673b6-147">Protocol specifications</span></span>

<span data-ttu-id="673b6-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="673b6-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="673b6-149">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="673b6-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="673b6-150">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="673b6-150">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="673b6-151">Spécifie l’emplacement et les propriétés des données de configuration client et serveur, telles que des listes de catégorie partagée et les heures de travail.</span><span class="sxs-lookup"><span data-stu-id="673b6-151">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="673b6-152">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="673b6-152">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="673b6-153">Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="673b6-153">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="673b6-154">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="673b6-154">Header files</span></span>

<span data-ttu-id="673b6-155">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="673b6-155">Mapidefs.h</span></span>
  
> <span data-ttu-id="673b6-156">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="673b6-156">Provides data type definitions.</span></span>
    
<span data-ttu-id="673b6-157">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="673b6-157">Mapitags.h</span></span>
  
> <span data-ttu-id="673b6-158">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="673b6-158">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="673b6-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="673b6-159">See also</span></span>

- [<span data-ttu-id="673b6-160">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="673b6-160">MAPI Properties</span></span>](mapi-properties.md)
- [<span data-ttu-id="673b6-161">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="673b6-161">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="673b6-162">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="673b6-162">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="673b6-163">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="673b6-163">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

