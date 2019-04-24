---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 17e900ac28481388379133a95b4b206ca4bc1805
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318423"
---
# <a name="attowner"></a><span data-ttu-id="b0c2b-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="b0c2b-103">attOwner</span></span>

  
  
<span data-ttu-id="b0c2b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0c2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0c2b-105">L'attribut **attOwner** est encodé sous la forme de chaînes comptées, de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="b0c2b-106">Le format de **attOwner** est le suivant:</span><span class="sxs-lookup"><span data-stu-id="b0c2b-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="b0c2b-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="b0c2b-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="b0c2b-108">Display-Name-longueur nom d'affichage-adresse de _messagerie_ -longueur adresse</span><span class="sxs-lookup"><span data-stu-id="b0c2b-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="b0c2b-109">_adresse de messagerie_</span><span class="sxs-lookup"><span data-stu-id="b0c2b-109">_email-address_</span></span>
  
> <span data-ttu-id="b0c2b-110">type **:** adresse</span><span class="sxs-lookup"><span data-stu-id="b0c2b-110">type **:** address</span></span> 
    
<span data-ttu-id="b0c2b-111">Contrairement à d'autres valeurs de longueur, la longueur de nom d'affichage et la longueur d'adresse sont des valeurs 16 bits non signées au lieu d'entiers longs non signés.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="b0c2b-112">Toutefois, ils incluent toujours des caractères nuls de fin.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="b0c2b-113">Les chaînes de type et d'adresse dans l'entrée _email-address_ sont séparées par un signe deux-points (:) caractère, tel que «SMTP:Joe@nowhere.com».</span><span class="sxs-lookup"><span data-stu-id="b0c2b-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="b0c2b-114">Seul le type combiné **:** la chaîne d'adresse est terminée par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="b0c2b-115">Le mappage des propriétés MAPI sur l'attribut **attOwner** dépend de la classe de message du message en cours de codage.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

