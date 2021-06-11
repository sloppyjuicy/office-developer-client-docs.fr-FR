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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2da826fe7ab9e4d7ca3eaaf0f9806193c47100d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315490"
---
# <a name="pidlidinternetaccountname-canonical-property"></a><span data-ttu-id="abcab-103">Propriété canonique PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="abcab-103">PidLidInternetAccountName Canonical Property</span></span>

  
  
<span data-ttu-id="abcab-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abcab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abcab-105">Spécifie le nom du compte de messagerie visible par l’utilisateur par le biais duquel le message électronique est envoyé.</span><span class="sxs-lookup"><span data-stu-id="abcab-105">Specifies the user-visible email account name through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abcab-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="abcab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="abcab-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="abcab-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="abcab-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="abcab-108">Property set:</span></span>  <br/> |<span data-ttu-id="abcab-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="abcab-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="abcab-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="abcab-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="abcab-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="abcab-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="abcab-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="abcab-112">Data type:</span></span>  <br/> |<span data-ttu-id="abcab-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="abcab-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="abcab-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="abcab-114">Area:</span></span>  <br/> |<span data-ttu-id="abcab-115">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="abcab-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abcab-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="abcab-116">Remarks</span></span>

<span data-ttu-id="abcab-117">Le format de cette chaîne dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="abcab-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="abcab-118">Cette propriété peut être utilisée par le client pour déterminer le serveur vers lequel diriger le courrier, mais elle est facultative et la valeur n’a aucune signification pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="abcab-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="abcab-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="abcab-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="abcab-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="abcab-120">Protocol specifications</span></span>

<span data-ttu-id="abcab-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abcab-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abcab-122">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="abcab-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="abcab-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abcab-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abcab-124">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="abcab-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="abcab-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="abcab-125">Header files</span></span>

<span data-ttu-id="abcab-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="abcab-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="abcab-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="abcab-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abcab-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abcab-128">See also</span></span>



[<span data-ttu-id="abcab-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="abcab-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="abcab-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="abcab-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="abcab-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="abcab-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="abcab-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="abcab-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

