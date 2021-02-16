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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415053"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="fae0c-103">Propriété canonique PidTagReceiveFolderSettings</span><span class="sxs-lookup"><span data-stu-id="fae0c-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="fae0c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fae0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fae0c-105">Contient une table des paramètres de dossier de réception d’une boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="fae0c-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fae0c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="fae0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fae0c-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="fae0c-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="fae0c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="fae0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fae0c-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="fae0c-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="fae0c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="fae0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="fae0c-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="fae0c-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="fae0c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="fae0c-112">Area:</span></span>  <br/> |<span data-ttu-id="fae0c-113">Magasin de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="fae0c-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fae0c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fae0c-114">Remarks</span></span>

<span data-ttu-id="fae0c-115">Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations [IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="fae0c-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="fae0c-116">En tant que propriété de type PT_OBJECT, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ; Son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) demandant l’interface avec l’identificateur IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="fae0c-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="fae0c-117">Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peuvent éventuellement la signaler ou non si elle n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="fae0c-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="fae0c-118">Pour récupérer le contenu de la table, une application cliente doit appeler la méthode [IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md)</span><span class="sxs-lookup"><span data-stu-id="fae0c-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="fae0c-119">Pour plus d’informations, voir [Tables des dossiers de réception.](receive-folder-tables.md)</span><span class="sxs-lookup"><span data-stu-id="fae0c-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="fae0c-120">Cette propriété contient une table des mappages des dossiers de réception pour la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="fae0c-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="fae0c-121">Appeler **OpenProperty sur** cette propriété équivaut à appeler **GetReceiveFolderTable** sur la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="fae0c-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fae0c-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="fae0c-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fae0c-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="fae0c-123">Header files</span></span>

<span data-ttu-id="fae0c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fae0c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="fae0c-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="fae0c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="fae0c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fae0c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="fae0c-127">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="fae0c-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fae0c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fae0c-128">See also</span></span>



[<span data-ttu-id="fae0c-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="fae0c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fae0c-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="fae0c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fae0c-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="fae0c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fae0c-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="fae0c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

