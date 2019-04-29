---
title: Propriété canonique PidTagAccessControlListTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424503"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a><span data-ttu-id="3dcd5-103">Propriété canonique PidTagAccessControlListTable</span><span class="sxs-lookup"><span data-stu-id="3dcd5-103">PidTagAccessControlListTable Canonical Property</span></span>

  
  
<span data-ttu-id="3dcd5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dcd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dcd5-105">Contient un tableau qui se compose de toutes les listes de contrôle d'accès système appliquées à un dossier.</span><span class="sxs-lookup"><span data-stu-id="3dcd5-105">Contains a table that consists of all the system access control lists (SACL) applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3dcd5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3dcd5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3dcd5-107">PR_ACL_TABLE</span><span class="sxs-lookup"><span data-stu-id="3dcd5-107">PR_ACL_TABLE</span></span>  <br/> |
|<span data-ttu-id="3dcd5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3dcd5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3dcd5-109">0x3FE0</span><span class="sxs-lookup"><span data-stu-id="3dcd5-109">0x3FE0</span></span>  <br/> |
|<span data-ttu-id="3dcd5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3dcd5-110">Data type:</span></span>  <br/> |<span data-ttu-id="3dcd5-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="3dcd5-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="3dcd5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3dcd5-112">Area:</span></span>  <br/> |<span data-ttu-id="3dcd5-113">Contrôle d'accès</span><span class="sxs-lookup"><span data-stu-id="3dcd5-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3dcd5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3dcd5-114">Remarks</span></span>

<span data-ttu-id="3dcd5-115">Cette propriété est présente sur tous les objets Folder sur un serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="3dcd5-115">This property is present on all folder objects on an Exchange Server.</span></span> <span data-ttu-id="3dcd5-116">Les valeurs comprises dans cette propriété sont utilisées pour la lecture et la modification de listes de contrôle d'accès (ACL) sur les dossiers.</span><span class="sxs-lookup"><span data-stu-id="3dcd5-116">Values included in this property are used for reading and modifying access control lists (ACLs) on folders.</span></span> <span data-ttu-id="3dcd5-117">Vous pouvez utiliser la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) avec l'identificateur d'interface **IID_IExchangeModifyTable** pour obtenir une interface [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) dans la table ACL d'un dossier.</span><span class="sxs-lookup"><span data-stu-id="3dcd5-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder.</span></span> <span data-ttu-id="3dcd5-118">Vous pouvez utiliser cette interface pour lire et modifier ces listes de Contrã'le d'accès.</span><span class="sxs-lookup"><span data-stu-id="3dcd5-118">You can use this interface to read and modify those ACLs.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3dcd5-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3dcd5-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3dcd5-120">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="3dcd5-120">Header files</span></span>

<span data-ttu-id="3dcd5-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3dcd5-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="3dcd5-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3dcd5-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="3dcd5-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3dcd5-123">Mapitags.h</span></span>
  
> <span data-ttu-id="3dcd5-124">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="3dcd5-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3dcd5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3dcd5-125">See also</span></span>



[<span data-ttu-id="3dcd5-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3dcd5-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3dcd5-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3dcd5-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3dcd5-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3dcd5-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3dcd5-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3dcd5-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

