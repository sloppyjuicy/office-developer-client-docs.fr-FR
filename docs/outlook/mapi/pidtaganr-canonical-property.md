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
ms.openlocfilehash: ce08ba971662b7f5060e6b24a6d2c5ee1a921d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327964"
---
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="5250f-103">Propriété canonique PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="5250f-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="5250f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5250f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5250f-105">Contient une valeur de chaîne à utiliser dans une restriction de propriété sur une table des matières du conteneur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="5250f-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5250f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5250f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5250f-107">PR_ANR, PR_ANR_A, PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="5250f-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="5250f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5250f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5250f-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="5250f-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="5250f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5250f-110">Data type:</span></span>  <br/> |<span data-ttu-id="5250f-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="5250f-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="5250f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5250f-112">Area:</span></span>  <br/> |<span data-ttu-id="5250f-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="5250f-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5250f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5250f-114">Remarks</span></span>

<span data-ttu-id="5250f-115">Ces propriétés n'appartiennent à aucun objet; Il est fourni par les fournisseurs de carnets d'adresses dans les structures [SPropertyRestriction](spropertyrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="5250f-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="5250f-116">Cette propriété contient une chaîne de résolution de noms ambiguë (ANR) pouvant être testée par rapport à la table des matières d'un conteneur de carnet d'adresses pour rechercher les destinataires de messages correspondants.</span><span class="sxs-lookup"><span data-stu-id="5250f-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="5250f-117">Les fournisseurs de carnet d'adresses correspondent à la valeur de **PR_ANR** et des propriétés associées par rapport à chaque entrée de la table de contenu, à l'aide d'un algorithme de correspondance défini par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5250f-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="5250f-118">La ou les colonnes utilisées dans cette correspondance sont choisies par le fournisseur dans le cadre de l'algorithme.</span><span class="sxs-lookup"><span data-stu-id="5250f-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="5250f-119">La colonne **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est la plus couramment utilisée; la colonne **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) est également utile lorsqu'elle contient le nom de messagerie de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5250f-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="5250f-120">Pour plus d'informations sur la résolution de noms ambiguës, consultez la rubrique [restrictions du carnet d'adresses](address-book-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="5250f-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5250f-121">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="5250f-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5250f-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="5250f-122">Protocol specifications</span></span>

<span data-ttu-id="5250f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5250f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5250f-124">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="5250f-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5250f-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5250f-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5250f-126">Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="5250f-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5250f-127">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="5250f-127">Header files</span></span>

<span data-ttu-id="5250f-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5250f-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5250f-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5250f-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="5250f-130">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5250f-130">Mapitags.h</span></span>
  
> <span data-ttu-id="5250f-131">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="5250f-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5250f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5250f-132">See also</span></span>



[<span data-ttu-id="5250f-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="5250f-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="5250f-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="5250f-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="5250f-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5250f-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5250f-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5250f-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5250f-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5250f-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5250f-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5250f-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

