---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408837"
---
# <a name="attsentfor"></a><span data-ttu-id="8c766-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="8c766-103">attSentFor</span></span>

  
  
<span data-ttu-id="8c766-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c766-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c766-105">L'attribut **attSentFor** est encodé sous la forme de chaînes comptées, de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="8c766-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="8c766-106">Le format de **attSentFor** est le suivant:</span><span class="sxs-lookup"><span data-stu-id="8c766-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="8c766-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="8c766-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="8c766-108">Display-Name-longueur nom d'affichage-adresse de _messagerie_ -longueur adresse</span><span class="sxs-lookup"><span data-stu-id="8c766-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="8c766-109">_adresse de messagerie_</span><span class="sxs-lookup"><span data-stu-id="8c766-109">_email-address_</span></span>
  
> <span data-ttu-id="8c766-110">type **:** adresse</span><span class="sxs-lookup"><span data-stu-id="8c766-110">type **:** address</span></span> 
    
<span data-ttu-id="8c766-111">Contrairement à d'autres valeurs de longueur, la longueur de nom d'affichage et la longueur d'adresse sont des valeurs 16 bits non signées au lieu d'entiers longs non signés.</span><span class="sxs-lookup"><span data-stu-id="8c766-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="8c766-112">Toutefois, ils incluent toujours des caractères nuls de fin.</span><span class="sxs-lookup"><span data-stu-id="8c766-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="8c766-113">Les chaînes de type et d'adresse dans l'entrée _email-address_ sont séparées par un signe deux-points (:) caractère, tel que «SMTP:Joe@nowhere.com».</span><span class="sxs-lookup"><span data-stu-id="8c766-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="8c766-114">Seul le type combiné **:** la chaîne d'adresse est terminée par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="8c766-114">Only the combined type **:** address string is null-terminated.</span></span>
  

