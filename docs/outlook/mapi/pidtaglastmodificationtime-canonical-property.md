---
title: Propriété canonique PidTagLastModificationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dea709b457e28efef62718fc388621e01c4eb5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279708"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a><span data-ttu-id="9bbee-103">Propriété canonique PidTagLastModificationTime</span><span class="sxs-lookup"><span data-stu-id="9bbee-103">PidTagLastModificationTime Canonical Property</span></span>

  
  
<span data-ttu-id="9bbee-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bbee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bbee-105">Contient la date et l’heure de la dernière modification de l’objet ou du sous-objet.</span><span class="sxs-lookup"><span data-stu-id="9bbee-105">Contains the date and time when the object or subobject was last modified.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9bbee-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9bbee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9bbee-107">PR_LAST_MODIFICATION_TIME</span><span class="sxs-lookup"><span data-stu-id="9bbee-107">PR_LAST_MODIFICATION_TIME</span></span>  <br/> |
|<span data-ttu-id="9bbee-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9bbee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9bbee-109">0x3008</span><span class="sxs-lookup"><span data-stu-id="9bbee-109">0x3008</span></span>  <br/> |
|<span data-ttu-id="9bbee-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9bbee-110">Data type:</span></span>  <br/> |<span data-ttu-id="9bbee-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="9bbee-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="9bbee-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9bbee-112">Area:</span></span>  <br/> |<span data-ttu-id="9bbee-113">Heure du message</span><span class="sxs-lookup"><span data-stu-id="9bbee-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bbee-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9bbee-114">Remarks</span></span>

<span data-ttu-id="9bbee-115">Cette propriété est initialement définie sur la même valeur que la **propriété PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9bbee-115">This property is initially set to the same value as the **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) property.</span></span> <span data-ttu-id="9bbee-116">Les sous-objets de pièce jointe peuvent le mettre à jour si nécessaire en copiant l’heure de la dernière modification conservée par le système de fichiers natif.</span><span class="sxs-lookup"><span data-stu-id="9bbee-116">Attachment subobjects can update it as necessary by copying the last modification time maintained by the native file system.</span></span> <span data-ttu-id="9bbee-117">Une application cliente peut définir cette propriété jusqu’au premier appel de la [méthode IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="9bbee-117">A client application can set this property until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="9bbee-118">À partir de là, le fournisseur doit mettre PR_LAST_MODIFICATION_TIME jour **pendant** chaque **appel IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="9bbee-118">From then on the provider should update **PR_LAST_MODIFICATION_TIME** during every **IMAPIProp::SaveChanges** call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9bbee-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9bbee-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9bbee-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="9bbee-120">Protocol specifications</span></span>

<span data-ttu-id="9bbee-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bbee-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bbee-122">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="9bbee-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9bbee-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bbee-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bbee-124">Gère la synchronisation des données d’objet de messagerie entre un serveur et un client.</span><span class="sxs-lookup"><span data-stu-id="9bbee-124">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="9bbee-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bbee-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bbee-126">Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="9bbee-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9bbee-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9bbee-127">Header files</span></span>

<span data-ttu-id="9bbee-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9bbee-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="9bbee-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9bbee-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="9bbee-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9bbee-130">Mapitags.h</span></span>
  
> <span data-ttu-id="9bbee-131">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="9bbee-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bbee-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bbee-132">See also</span></span>



[<span data-ttu-id="9bbee-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9bbee-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9bbee-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9bbee-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9bbee-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9bbee-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9bbee-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9bbee-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

