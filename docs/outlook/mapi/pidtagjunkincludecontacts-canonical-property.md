---
title: Propriété canonique PidTagJunkIncludeContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7e61e98d1db1ab3acb958da353d8d22870937632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328713"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a><span data-ttu-id="5d2e6-103">Propriété canonique PidTagJunkIncludeContacts</span><span class="sxs-lookup"><span data-stu-id="5d2e6-103">PidTagJunkIncludeContacts Canonical Property</span></span>

  
  
<span data-ttu-id="5d2e6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d2e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d2e6-105">Indique si les adresses e-mail des contacts dans le dossier Contacts sont traitées spécialement par rapport au filtre de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="5d2e6-105">Indicates whether email addresses of the contacts in the Contacts folder are treated specially with respect to the spam filter.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d2e6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5d2e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d2e6-107">PR_JUNK_INCLUDE_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="5d2e6-107">PR_JUNK_INCLUDE_CONTACTS</span></span>  <br/> |
|<span data-ttu-id="5d2e6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5d2e6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d2e6-109">0x6100</span><span class="sxs-lookup"><span data-stu-id="5d2e6-109">0x6100</span></span>  <br/> |
|<span data-ttu-id="5d2e6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5d2e6-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d2e6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5d2e6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5d2e6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5d2e6-112">Area:</span></span>  <br/> |<span data-ttu-id="5d2e6-113">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="5d2e6-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d2e6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d2e6-114">Remarks</span></span>

<span data-ttu-id="5d2e6-115">Si la propriété est définie sur « 0x00000001 », ces adresses de messagerie doivent remplir la partie « adresse e-mail de contact approuvé » de la restriction de règle de courrier indésirable afin que le courrier provenant de ces adresses soit considéré comme « non indésirable ».</span><span class="sxs-lookup"><span data-stu-id="5d2e6-115">If set to "0x00000001", these email addresses must populate the "trusted" contact email address portion of the Junk E-Mail Rule Restriction such that mail from these addresses is treated as "not junk".</span></span> <span data-ttu-id="5d2e6-116">Si la valeur est « 0x00000000 », les adresses de messagerie du dossier Contacts ne doivent pas être ajoutées à la règle de courrier indésirable et la section de la règle doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="5d2e6-116">If set to "0x00000000", email addresses from the Contacts folder must not be added to the Junk E-Mail Rule, and the section of the rule must be NULL.</span></span>
  
<span data-ttu-id="5d2e6-117">Si cette propriété est présente avec la valeur « 0x00000001 » et si le contact ajouté a des adresses de messagerie qui ne sont pas encore incluses dans la section contacts de confiance de la règle de courrier indésirable, ces adresses de messagerie doivent être ajoutées à la restriction.</span><span class="sxs-lookup"><span data-stu-id="5d2e6-117">If this property is present with a value of "0x00000001" and if the added contact has email addresses that are not yet included in the trusted contacts section of the Junk E-Mail Rule, those email addresses must be added to the restriction.</span></span> <span data-ttu-id="5d2e6-118">Si cette propriété est « 0x00000000 », aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="5d2e6-118">If this property is "0x00000000", no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5d2e6-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5d2e6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d2e6-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="5d2e6-120">Protocol specifications</span></span>

<span data-ttu-id="5d2e6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d2e6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d2e6-122">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="5d2e6-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5d2e6-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d2e6-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d2e6-124">Permet la gestion des listes d’adresses de courriers indésirables et la détermination des messages électroniques indésirables.</span><span class="sxs-lookup"><span data-stu-id="5d2e6-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d2e6-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5d2e6-125">Header files</span></span>

<span data-ttu-id="5d2e6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d2e6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d2e6-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5d2e6-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="5d2e6-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5d2e6-128">Mapitags.h</span></span>
  
> <span data-ttu-id="5d2e6-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="5d2e6-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d2e6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d2e6-130">See also</span></span>



[<span data-ttu-id="5d2e6-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5d2e6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d2e6-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5d2e6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d2e6-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5d2e6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d2e6-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5d2e6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

