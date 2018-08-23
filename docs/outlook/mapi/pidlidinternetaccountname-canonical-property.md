---
title: Propriété canonique PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountName
api_type:
- COM
ms.assetid: 29bedadf-903d-419d-804d-dc8bd92b745d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ac47f150ebdd39ed5f2abe4b30a2cac5768fd229
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565129"
---
# <a name="pidlidinternetaccountname-canonical-property"></a><span data-ttu-id="f93e9-103">Propriété canonique PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="f93e9-103">PidLidInternetAccountName Canonical Property</span></span>

  
  
<span data-ttu-id="f93e9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f93e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f93e9-105">Spécifie le nom du compte de messagerie visible par l’utilisateur à travers lequel le message électronique est envoyé.</span><span class="sxs-lookup"><span data-stu-id="f93e9-105">Specifies the user-visible email account name through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f93e9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f93e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f93e9-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="f93e9-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="f93e9-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="f93e9-108">Property set:</span></span>  <br/> |<span data-ttu-id="f93e9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f93e9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f93e9-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="f93e9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f93e9-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="f93e9-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="f93e9-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f93e9-112">Data type:</span></span>  <br/> |<span data-ttu-id="f93e9-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f93e9-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f93e9-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f93e9-114">Area:</span></span>  <br/> |<span data-ttu-id="f93e9-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="f93e9-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f93e9-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f93e9-116">Remarks</span></span>

<span data-ttu-id="f93e9-117">Le format de cette chaîne est dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="f93e9-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="f93e9-118">Cette propriété peut être utilisée par le client pour déterminer le serveur pour diriger la messagerie, mais est facultative et la valeur est dépourvu de signification sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="f93e9-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f93e9-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f93e9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f93e9-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f93e9-120">Protocol specifications</span></span>

<span data-ttu-id="f93e9-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f93e9-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f93e9-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="f93e9-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f93e9-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f93e9-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f93e9-124">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="f93e9-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f93e9-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f93e9-125">Header files</span></span>

<span data-ttu-id="f93e9-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f93e9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f93e9-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f93e9-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f93e9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f93e9-128">See also</span></span>



[<span data-ttu-id="f93e9-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f93e9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f93e9-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f93e9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f93e9-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f93e9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f93e9-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f93e9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

