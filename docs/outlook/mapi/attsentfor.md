---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318115"
---
# <a name="attsentfor"></a><span data-ttu-id="1b817-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="1b817-103">attSentFor</span></span>

  
  
<span data-ttu-id="1b817-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b817-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b817-105">L'attribut **attSentFor** est encodé sous la forme de chaînes comptées, de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="1b817-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="1b817-106">Le format de **attSentFor** est le suivant:</span><span class="sxs-lookup"><span data-stu-id="1b817-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="1b817-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="1b817-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="1b817-108">Display-Name-longueur nom d'affichage-adresse de _messagerie_ -longueur adresse</span><span class="sxs-lookup"><span data-stu-id="1b817-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="1b817-109">_adresse de messagerie_</span><span class="sxs-lookup"><span data-stu-id="1b817-109">_email-address_</span></span>
  
> <span data-ttu-id="1b817-110">type **:** adresse</span><span class="sxs-lookup"><span data-stu-id="1b817-110">type **:** address</span></span> 
    
<span data-ttu-id="1b817-111">Contrairement à d'autres valeurs de longueur, la longueur de nom d'affichage et la longueur d'adresse sont des valeurs 16 bits non signées au lieu d'entiers longs non signés.</span><span class="sxs-lookup"><span data-stu-id="1b817-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="1b817-112">Toutefois, ils incluent toujours des caractères nuls de fin.</span><span class="sxs-lookup"><span data-stu-id="1b817-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="1b817-113">Les chaînes de type et d'adresse dans l'entrée _email-address_ sont séparées par un signe deux-points (:) caractère, tel que «SMTP:Joe@nowhere.com».</span><span class="sxs-lookup"><span data-stu-id="1b817-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="1b817-114">Seul le type combiné **:** la chaîne d'adresse est terminée par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="1b817-114">Only the combined type **:** address string is null-terminated.</span></span>
  

