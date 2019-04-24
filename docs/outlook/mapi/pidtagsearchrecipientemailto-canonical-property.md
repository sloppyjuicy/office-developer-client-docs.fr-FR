---
title: Propriété canonique PidTagSearchRecipientEmailTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d254df132db5542ce5235c1c3ab42ea768399f0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358918"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a><span data-ttu-id="7612c-103">Propriété canonique PidTagSearchRecipientEmailTo</span><span class="sxs-lookup"><span data-stu-id="7612c-103">PidTagSearchRecipientEmailTo Canonical Property</span></span>

  
  
<span data-ttu-id="7612c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7612c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7612c-105">Contient une chaîne Unicode interrogée dans la liste des adresses de messagerie ou des noms d'affichage des destinataires qui sont traités dans la ligne **à** des messages de la Banque.</span><span class="sxs-lookup"><span data-stu-id="7612c-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **To** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="7612c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7612c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7612c-107">PR_SEARCH_RECIP_EMAIL_TO_W</span><span class="sxs-lookup"><span data-stu-id="7612c-107">PR_SEARCH_RECIP_EMAIL_TO_W</span></span>  <br/> |
|<span data-ttu-id="7612c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7612c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7612c-109">0x0EA6</span><span class="sxs-lookup"><span data-stu-id="7612c-109">0x0EA6</span></span>  <br/> |
|<span data-ttu-id="7612c-110">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="7612c-110">Property type:</span></span>  <br/> |<span data-ttu-id="7612c-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7612c-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7612c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="7612c-112">Area:</span></span>  <br/> |<span data-ttu-id="7612c-113">Rechercher</span><span class="sxs-lookup"><span data-stu-id="7612c-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7612c-114">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="7612c-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="7612c-115">Cette balise de restriction MAPI, utilisée lorsque vous recherchez des adresses de messagerie ou des noms d'affichage auxquels le message est envoyé, ne peut pas être définie dans le fichier d'en-tête téléchargeable dont vous disposez actuellement.</span><span class="sxs-lookup"><span data-stu-id="7612c-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="7612c-116">Vous pouvez l'ajouter à votre code à l'aide de la valeur suivante: >`#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span><span class="sxs-lookup"><span data-stu-id="7612c-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="7612c-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="7612c-117">Protocol specifications</span></span>

<span data-ttu-id="7612c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7612c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7612c-119">Fournit des références aux spécifications de protocole Microsoft Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="7612c-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7612c-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7612c-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7612c-121">Spécifie les propriétés et les opérations pour la manipulation d'une configuration de liste des dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="7612c-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7612c-122">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="7612c-122">Header files</span></span>

<span data-ttu-id="7612c-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7612c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7612c-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7612c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7612c-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7612c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7612c-126">Contient les définitions des propriétés qui sont répertoriées en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="7612c-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7612c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7612c-127">See also</span></span>



[<span data-ttu-id="7612c-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7612c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7612c-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7612c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7612c-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7612c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7612c-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="7612c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

