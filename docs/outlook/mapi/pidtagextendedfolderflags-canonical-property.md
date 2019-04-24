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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fe14f6ca101e6a546f99989ecc87b0c516ee5df4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316351"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a><span data-ttu-id="5c4ca-103">Propriété canonique PidTagExtendedFolderFlags</span><span class="sxs-lookup"><span data-stu-id="5c4ca-103">PidTagExtendedFolderFlags Canonical Property</span></span>
 
<span data-ttu-id="5c4ca-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c4ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c4ca-105">Contient des indicateurs étendus relatifs à un dossier.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-105">Contains extended flags about a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c4ca-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5c4ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c4ca-107">PR_EXTENDED_FOLDER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="5c4ca-107">PR_EXTENDED_FOLDER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="5c4ca-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5c4ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5c4ca-109">0x36DA</span><span class="sxs-lookup"><span data-stu-id="5c4ca-109">0x36DA</span></span>  <br/> |
|<span data-ttu-id="5c4ca-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5c4ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="5c4ca-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5c4ca-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5c4ca-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5c4ca-112">Area:</span></span>  <br/> |<span data-ttu-id="5c4ca-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="5c4ca-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c4ca-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5c4ca-114">Remarks</span></span>

<span data-ttu-id="5c4ca-115">Cette propriété est un flux binaire qui contient des sous-propriétés codées pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-115">This property is a binary stream that contains encoded sub-properties for the folder.</span></span> <span data-ttu-id="5c4ca-116">Elle est mise en forme comme une série d'éléments secondaires de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-116">It is formatted as a series of variable length sub items.</span></span> <span data-ttu-id="5c4ca-117">Les 8 premiers bits du sous-élément sont un champ ID, qui indique le type d'indicateur représenté par le sous-élément.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-117">The first 8 bits of the sub item is an ID field, which indicates what kind of flag the sub item represents.</span></span> <span data-ttu-id="5c4ca-118">Le deuxième 8 bits est le nombre d'octets de données qui suivent.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-118">The second 8 bits is the number of bytes of data that follow.</span></span>
  
<span data-ttu-id="5c4ca-119">Les valeurs d'ID possibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="5c4ca-119">Possible ID values include:</span></span>
  
- <span data-ttu-id="5c4ca-120">Invalid</span><span class="sxs-lookup"><span data-stu-id="5c4ca-120">Invalid</span></span>
    
   <span data-ttu-id="5c4ca-121">Ne pas utiliser cette valeur</span><span class="sxs-lookup"><span data-stu-id="5c4ca-121">Do not use this value</span></span>
    
- <span data-ttu-id="5c4ca-122">ExtendedFlags</span><span class="sxs-lookup"><span data-stu-id="5c4ca-122">ExtendedFlags</span></span>
    
   <span data-ttu-id="5c4ca-123">Les données sont une valeur de quatre octets formatée comme suit:</span><span class="sxs-lookup"><span data-stu-id="5c4ca-123">The data is a four byte value formatted as:</span></span>
    
   |<span data-ttu-id="5c4ca-124">**Bits**</span><span class="sxs-lookup"><span data-stu-id="5c4ca-124">**Bits**</span></span>|<span data-ttu-id="5c4ca-125">**Description**</span><span class="sxs-lookup"><span data-stu-id="5c4ca-125">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="5c4ca-126">0-1</span><span class="sxs-lookup"><span data-stu-id="5c4ca-126">0-1</span></span>  <br/> |<span data-ttu-id="5c4ca-127">Réservé.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-127">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="5c4ca-128">n°2</span><span class="sxs-lookup"><span data-stu-id="5c4ca-128">2</span></span>  <br/> |<span data-ttu-id="5c4ca-129">Affectez la valeur 0 si l'application doit afficher une description de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-129">Set to 0 if the application should show a policy description.</span></span>  <br/> |
   |<span data-ttu-id="5c4ca-130">3-5</span><span class="sxs-lookup"><span data-stu-id="5c4ca-130">3-5</span></span>  <br/> |<span data-ttu-id="5c4ca-131">Réservé.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-131">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="5c4ca-132">6-7</span><span class="sxs-lookup"><span data-stu-id="5c4ca-132">6-7</span></span>  <br/> |<span data-ttu-id="5c4ca-133">Contrôle l'affichage du nombre de messages dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-133">Controls the display of the number of messages in the folder.</span></span>  <br/> <span data-ttu-id="5c4ca-134">0-utiliser le paramètre par défaut</span><span class="sxs-lookup"><span data-stu-id="5c4ca-134">0 - Use the default setting</span></span>  <br/> <span data-ttu-id="5c4ca-135">1-utiliser le nombre de messages non lus</span><span class="sxs-lookup"><span data-stu-id="5c4ca-135">1 - Use the number of unread messages</span></span>  <br/> <span data-ttu-id="5c4ca-136">3-utiliser le nombre total de messages</span><span class="sxs-lookup"><span data-stu-id="5c4ca-136">3 - Use the total number of messages</span></span>  <br/> |
   |<span data-ttu-id="5c4ca-137">8-31</span><span class="sxs-lookup"><span data-stu-id="5c4ca-137">8-31</span></span>  <br/> |<span data-ttu-id="5c4ca-138">Réservé.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-138">Reserved.</span></span>  <br/> |
   
<span data-ttu-id="5c4ca-139">Les éléments réservés peuvent être ignorés, mais les valeurs existantes doivent être conservées.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-139">Reserved items can be ignored, but existing values must be preserved.</span></span>
    
- <span data-ttu-id="5c4ca-140">SearchFolderID</span><span class="sxs-lookup"><span data-stu-id="5c4ca-140">SearchFolderID</span></span>
    
   <span data-ttu-id="5c4ca-141">Le champ de données est un champ de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-141">The data field is a 16-byte field.</span></span> <span data-ttu-id="5c4ca-142">Lorsque l'application crée un dossier de recherche persistante, elle doit définir ce champ dans le dossier sur la même valeur que la propriété binaire **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) sur le message du dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-142">When the application creates a persistent search folder, it must set this field on the folder to the same value as the **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binary property on the Search Folder Message.</span></span>
    
- <span data-ttu-id="5c4ca-143">ToDoFolderVersion</span><span class="sxs-lookup"><span data-stu-id="5c4ca-143">ToDoFolderVersion</span></span>
    
   <span data-ttu-id="5c4ca-144">Le champ de données est un champ de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-144">The data field is a 4-byte field.</span></span> <span data-ttu-id="5c4ca-145">Lorsque l'application crée le dossier de recherche de tâches, elle doit définir la valeur de ce champ sur le dossier sur la valeur entière Little-endian de «0x000c0000»:</span><span class="sxs-lookup"><span data-stu-id="5c4ca-145">When the application creates the to-do search folder, it must set the value of this field on the folder to the little-endian integer value of" 0x000c0000":</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="5c4ca-146">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="5c4ca-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c4ca-147">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="5c4ca-147">Protocol specifications</span></span>

<span data-ttu-id="5c4ca-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c4ca-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c4ca-149">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5c4ca-150">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c4ca-150">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c4ca-151">Spécifie l'emplacement et les propriétés des données de configuration du client et du serveur, telles que les listes de catégories partagées et les heures de travail.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-151">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="5c4ca-152">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c4ca-152">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c4ca-153">Spécifie les propriétés et les opérations pour la manipulation d'une configuration de liste des dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-153">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c4ca-154">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="5c4ca-154">Header files</span></span>

<span data-ttu-id="5c4ca-155">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5c4ca-155">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c4ca-156">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-156">Provides data type definitions.</span></span>
    
<span data-ttu-id="5c4ca-157">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5c4ca-157">Mapitags.h</span></span>
  
> <span data-ttu-id="5c4ca-158">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="5c4ca-158">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c4ca-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c4ca-159">See also</span></span>

- [<span data-ttu-id="5c4ca-160">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5c4ca-160">MAPI Properties</span></span>](mapi-properties.md)
- [<span data-ttu-id="5c4ca-161">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5c4ca-161">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="5c4ca-162">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5c4ca-162">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="5c4ca-163">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5c4ca-163">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

