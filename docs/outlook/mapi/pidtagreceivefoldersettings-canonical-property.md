---
title: Propriété canonique PidTagReceiveFolderSettings
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356741"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="f4e89-103">Propriété canonique PidTagReceiveFolderSettings</span><span class="sxs-lookup"><span data-stu-id="f4e89-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="f4e89-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4e89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4e89-105">Contient un tableau des paramètres de dossier de réception d'une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f4e89-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4e89-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f4e89-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4e89-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="f4e89-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="f4e89-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f4e89-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4e89-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="f4e89-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="f4e89-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f4e89-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4e89-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="f4e89-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="f4e89-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f4e89-112">Area:</span></span>  <br/> |<span data-ttu-id="f4e89-113">Banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="f4e89-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4e89-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f4e89-114">Remarks</span></span>

<span data-ttu-id="f4e89-115">Cette propriété peut être exclue dans [IMAPIProp:: CopyTo](imapiprop-copyto.md) Operations ou incluse dans [IMAPIProp:: CopyProps](imapiprop-copyprops.md) Operations.</span><span class="sxs-lookup"><span data-stu-id="f4e89-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="f4e89-116">En tant que propriété de type PT_OBJECT, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) ; son contenu doit être accessible à l'aide de la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , qui demande l'interface avec l'identificateur IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="f4e89-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="f4e89-117">Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) s'il est défini, mais peuvent éventuellement le signaler ou non s'il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f4e89-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="f4e89-118">Pour récupérer le contenu de la table, une application cliente doit appeler la méthode [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="f4e89-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="f4e89-119">Pour plus d'informations, consultez la rubrique [Receive Folder tables](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f4e89-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="f4e89-120">Cette propriété contient un tableau des mappages des dossiers de réception pour la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f4e89-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="f4e89-121">L'appel de **OpenProperty** sur cette propriété équivaut à l'appel de **GetReceiveFolderTable** sur la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f4e89-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f4e89-122">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="f4e89-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f4e89-123">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="f4e89-123">Header files</span></span>

<span data-ttu-id="f4e89-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f4e89-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4e89-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f4e89-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4e89-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f4e89-126">Mapitags.h</span></span>
  
> <span data-ttu-id="f4e89-127">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="f4e89-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4e89-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4e89-128">See also</span></span>



[<span data-ttu-id="f4e89-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f4e89-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4e89-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f4e89-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4e89-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f4e89-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4e89-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f4e89-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

