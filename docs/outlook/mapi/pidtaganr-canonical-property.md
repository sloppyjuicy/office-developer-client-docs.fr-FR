---
title: Propriété canonique PidTagAnr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 94e83f4a93bac4ee144c5fbf94fd4b3fdb6c2f55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785695"
---
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="85965-103">Propriété canonique PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="85965-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="85965-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="85965-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="85965-105">Contient une valeur de chaîne pour une utilisation dans une restriction de propriété sur une table des matières adresses livre conteneur.</span><span class="sxs-lookup"><span data-stu-id="85965-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85965-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="85965-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="85965-107">PR_ANR, PR_ANR_A, PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="85965-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="85965-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="85965-108">Identifier:</span></span>  <br/> |<span data-ttu-id="85965-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="85965-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="85965-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="85965-110">Data type:</span></span>  <br/> |<span data-ttu-id="85965-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="85965-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="85965-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="85965-112">Area:</span></span>  <br/> |<span data-ttu-id="85965-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="85965-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85965-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="85965-114">Remarks</span></span>

<span data-ttu-id="85965-115">Ces propriétés n’appartiennent pas à n’importe quel objet ; Il est fourni par les fournisseurs de carnet d’adresses dans des structures [SPropertyRestriction](spropertyrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="85965-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="85965-116">Cette propriété contient une chaîne (ANR) de résolution de nom ambigu qui peut être testée par rapport à la table de contenu d’un conteneur carnet d’adresses pour rechercher les destinataires du message correspondant.</span><span class="sxs-lookup"><span data-stu-id="85965-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="85965-117">Fournisseurs de carnet d’adresses correspondent à la valeur de **PR_ANR** et des propriétés associées par rapport à chaque entrée dans la table des matières, à l’aide d’un algorithme de correspondance défini par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="85965-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="85965-118">L’ou les colonnes qui sont utilisés dans cette correspondance sont choisis par le fournisseur dans le cadre de l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="85965-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="85965-119">La colonne **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est le plus fréquemment utilisée ; la colonne **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) est également utile lorsqu’il contient le nom de l’utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="85965-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="85965-120">Pour plus d’informations sur la résolution de nom ambigu, consultez [Restrictions de carnet d’adresses](address-book-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="85965-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="85965-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="85965-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="85965-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="85965-122">Protocol specifications</span></span>

<span data-ttu-id="85965-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85965-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85965-124">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="85965-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="85965-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85965-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85965-126">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="85965-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="85965-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="85965-127">Header files</span></span>

<span data-ttu-id="85965-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="85965-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="85965-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="85965-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="85965-130">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="85965-130">Mapitags.h</span></span>
  
> <span data-ttu-id="85965-131">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="85965-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85965-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85965-132">See also</span></span>



[<span data-ttu-id="85965-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="85965-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="85965-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="85965-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="85965-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="85965-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="85965-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="85965-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="85965-137">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="85965-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="85965-138">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="85965-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

