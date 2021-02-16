---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 17e900ac28481388379133a95b4b206ca4bc1805
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427653"
---
# <a name="attowner"></a><span data-ttu-id="87ae7-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="87ae7-103">attOwner</span></span>

  
  
<span data-ttu-id="87ae7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87ae7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87ae7-105">**L’attribut attOwner** est codé en tant que chaînes comptées mises de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="87ae7-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="87ae7-106">Le format de **attOwner est** le suivant :</span><span class="sxs-lookup"><span data-stu-id="87ae7-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="87ae7-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="87ae7-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="87ae7-108">display-name-length display-name address-length  _email-address_</span><span class="sxs-lookup"><span data-stu-id="87ae7-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="87ae7-109">_email-address_</span><span class="sxs-lookup"><span data-stu-id="87ae7-109">_email-address_</span></span>
  
> <span data-ttu-id="87ae7-110">type **:** address</span><span class="sxs-lookup"><span data-stu-id="87ae7-110">type **:** address</span></span> 
    
<span data-ttu-id="87ae7-111">Contrairement aux autres valeurs de longueur, les longueurs de nom d’affichage et d’adresse sont des valeurs 16 bits non signées au lieu des nombres longs non signés.</span><span class="sxs-lookup"><span data-stu-id="87ae7-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="87ae7-112">Toutefois, elles incluent toujours des caractères null de fin.</span><span class="sxs-lookup"><span data-stu-id="87ae7-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="87ae7-113">Les chaînes de type et d’adresse dans l’entrée d’adresse de messagerie sont séparées par un  _deux-points_ littéral (:) par exemple« smtp:joe@nowhere.com ».</span><span class="sxs-lookup"><span data-stu-id="87ae7-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="87ae7-114">Seul le type combiné : **chaîne** d’adresse est terminée par null.</span><span class="sxs-lookup"><span data-stu-id="87ae7-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="87ae7-115">Le mappage des propriétés MAPI à **l’attribut attOwner** dépend de la classe de message du message en cours d’encodage.</span><span class="sxs-lookup"><span data-stu-id="87ae7-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

