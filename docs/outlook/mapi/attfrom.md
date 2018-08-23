---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6460cd3ef0495a5494e03b4c7034e067cf8793b7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576063"
---
# <a name="attfrom"></a><span data-ttu-id="b2de8-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="b2de8-103">attFrom</span></span>

<span data-ttu-id="b2de8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2de8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2de8-105">L’attribut **attFrom** est codé en une structure **TRP** qui encode l’adresse d’e-mail et le nom complet de l’expéditeur, suivi par le nom complet et l’adresse de l’expéditeur, suivi par n’importe quel remplissage nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b2de8-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="b2de8-106">Le format de **attFrom** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="b2de8-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="b2de8-107">**attFrom**: remplissage d’une _structure-TRP_ _ expéditeur nom d’affichage adresse d’expéditeur _</span><span class="sxs-lookup"><span data-stu-id="b2de8-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="b2de8-108">Le nom complet l’expéditeur est une chaîne qui est remplie par un caractère null supplémentaire, si nécessaire, pour atteindre une limite de 2 octets.</span><span class="sxs-lookup"><span data-stu-id="b2de8-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="b2de8-109">Le remplissage à la fin de la méthode de codage **attFrom** se compose de caractères de null autant que nécessaire pour atteindre une limite **sizeof(TRP)** .</span><span class="sxs-lookup"><span data-stu-id="b2de8-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="b2de8-110">_TRP-structure :_ **trpidOneOff** cbgrtrp cch cb</span><span class="sxs-lookup"><span data-stu-id="b2de8-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="b2de8-111">Pour l’élément **attFrom** , la **TRP**-structure est toujours un uniques codage, donc la trpid désactive le **TRP**-champ de la structure est toujours **trpidOneOff**.</span><span class="sxs-lookup"><span data-stu-id="b2de8-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="b2de8-112">Cbgrtrp, cch, les éléments cb correspondent aux champs restants de la structure **TRP** .</span><span class="sxs-lookup"><span data-stu-id="b2de8-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="b2de8-113">Le champ cbgrtrp est calculé comme la somme des **(sizeof(TRP) \*2)**, la longueur de caractère nul-affichage-nom de l’expéditeur avec son remplissage et la longueur de l’adresse expéditeur terminée.</span><span class="sxs-lookup"><span data-stu-id="b2de8-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="b2de8-114">Le champ cch est calculé en tant que la longueur du caractère nul-nom d’affichage avec son remplissage.</span><span class="sxs-lookup"><span data-stu-id="b2de8-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="b2de8-115">Le champ cb est calculé en tant que la longueur de l’adresse expéditeur terminée.</span><span class="sxs-lookup"><span data-stu-id="b2de8-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="b2de8-116">_-adresse de l’expéditeur :_ type d’adresse **:** adresse **'\0'**</span><span class="sxs-lookup"><span data-stu-id="b2de8-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="b2de8-117">L’adresse de l’expéditeur est une chaîne qui se compose de quatre parties, le type d’adresse, littéral (deux-points), l’adresse lui-même et un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="b2de8-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="b2de8-118">Par exemple, la chaîne `fax:1-909-555-1234\0` est une valeur de l’adresse de l’expéditeur juridique.</span><span class="sxs-lookup"><span data-stu-id="b2de8-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

