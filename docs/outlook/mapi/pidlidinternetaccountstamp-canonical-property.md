---
title: Propriété canonique PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountStamp
api_type:
- COM
ms.assetid: 819179fe-e58e-415c-abc7-1949036745ee
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ebd64392d24cd170a7babf77865aa00c7be24802
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315455"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a><span data-ttu-id="b91ff-103">Propriété canonique PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="b91ff-103">PidLidInternetAccountStamp Canonical Property</span></span>

  
  
<span data-ttu-id="b91ff-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b91ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b91ff-105">Spécifie l'ID de compte de messagerie par lequel le message électronique est envoyé.</span><span class="sxs-lookup"><span data-stu-id="b91ff-105">Specifies the email account ID through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b91ff-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b91ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b91ff-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="b91ff-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="b91ff-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="b91ff-108">Property set:</span></span>  <br/> |<span data-ttu-id="b91ff-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b91ff-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b91ff-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="b91ff-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b91ff-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="b91ff-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="b91ff-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b91ff-112">Data type:</span></span>  <br/> |<span data-ttu-id="b91ff-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b91ff-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b91ff-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b91ff-114">Area:</span></span>  <br/> |<span data-ttu-id="b91ff-115">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="b91ff-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b91ff-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b91ff-116">Remarks</span></span>

<span data-ttu-id="b91ff-117">Le format de cette chaîne est dépendant de l'implémentation.</span><span class="sxs-lookup"><span data-stu-id="b91ff-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="b91ff-118">Cette propriété peut être utilisée par le client pour déterminer à quel serveur diriger le courrier, mais elle est facultative et la valeur n'a aucune signification pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="b91ff-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b91ff-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="b91ff-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b91ff-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="b91ff-120">Protocol specifications</span></span>

<span data-ttu-id="b91ff-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b91ff-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b91ff-122">Fournit la définition des jeux de propriétés et les références aux spécifications du protocole Exchange Server associé.</span><span class="sxs-lookup"><span data-stu-id="b91ff-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b91ff-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b91ff-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b91ff-124">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="b91ff-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b91ff-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="b91ff-125">Header files</span></span>

<span data-ttu-id="b91ff-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b91ff-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b91ff-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b91ff-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b91ff-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b91ff-128">See also</span></span>



[<span data-ttu-id="b91ff-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b91ff-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b91ff-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b91ff-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b91ff-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b91ff-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b91ff-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b91ff-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

