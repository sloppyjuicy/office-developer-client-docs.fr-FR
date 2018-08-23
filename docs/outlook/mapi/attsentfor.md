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
ms.openlocfilehash: b292e65ddabcbe052832687a3dcf01658de5e379
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567474"
---
# <a name="attsentfor"></a><span data-ttu-id="6e674-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="6e674-103">attSentFor</span></span>

  
  
<span data-ttu-id="6e674-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e674-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e674-105">L’attribut **attSentFor** est codée selon les chaînes comptées bout en bout.</span><span class="sxs-lookup"><span data-stu-id="6e674-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="6e674-106">Le format de **attSentFor** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="6e674-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="6e674-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="6e674-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="6e674-108">longueur du nom d’affichage du nom d’affichage longueur adresse _adresse de messagerie_</span><span class="sxs-lookup"><span data-stu-id="6e674-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="6e674-109">_adresse de messagerie_</span><span class="sxs-lookup"><span data-stu-id="6e674-109">_email-address_</span></span>
  
> <span data-ttu-id="6e674-110">adresse de type **:**</span><span class="sxs-lookup"><span data-stu-id="6e674-110">type **:** address</span></span> 
    
<span data-ttu-id="6e674-111">Contrairement à d’autres longueur valeurs, la longueur du nom d’affichage et adresse longueur sont des valeurs de 16 bits non signées au lieu d’entiers longs non signés.</span><span class="sxs-lookup"><span data-stu-id="6e674-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="6e674-112">Elles incluent toujours abandon de caractères null, toutefois.</span><span class="sxs-lookup"><span data-stu-id="6e674-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="6e674-113">Les chaînes de type et l’adresse dans l’entrée _d’adresse de messagerie_ sont séparés par un caractère littéral (deux-points), tel que « smtp:joe@nowhere.com ».</span><span class="sxs-lookup"><span data-stu-id="6e674-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="6e674-114">Uniquement la chaîne d’adresse type combinée **:** est terminée.</span><span class="sxs-lookup"><span data-stu-id="6e674-114">Only the combined type **:** address string is null-terminated.</span></span>
  

