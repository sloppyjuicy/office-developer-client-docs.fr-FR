---
title: Format TNEF (Transport Neutral Encapsulation Format)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Dernière modification : 12 mars 2013'
ms.openlocfilehash: 440c27b019b91ec8c2c02e37850d2768a273559b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591932"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="74a10-103">Format TNEF (Transport Neutral Encapsulation Format)</span><span class="sxs-lookup"><span data-stu-id="74a10-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="74a10-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74a10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74a10-105">Le format TNEF est un format de conversion d’un jeu de propriétés MAPI — un message MAPI — dans un flux de données en série.</span><span class="sxs-lookup"><span data-stu-id="74a10-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="74a10-106">Les fonctions TNEF sont principalement utilisées par les fournisseurs de transport qui peut-être coder les propriétés de message MAPI pour la transmission via un système de messagerie qui ne prend pas en charge ces propriétés directement.</span><span class="sxs-lookup"><span data-stu-id="74a10-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="74a10-107">Par exemple, un type de transport basé sur SMTP utilise TNEF pour coder les propriétés comme **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), qui n’ont pas de représentations directes dans la structure d’un message SMTP.</span><span class="sxs-lookup"><span data-stu-id="74a10-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="74a10-108">L’implémentation TNEF définit plusieurs attributs spécifiques TNEF, chacun d'entre eux correspond à une propriété MAPI particulière.</span><span class="sxs-lookup"><span data-stu-id="74a10-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="74a10-109">Ces attributs sont utilisés pour coder leurs propriétés MAPI respectifs dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="74a10-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="74a10-110">En outre, un attribut spécial est défini pouvant être utilisés pour encapsuler des propriétés MAPI qui ne dispose pas d’un attribut spécifique correspondante.</span><span class="sxs-lookup"><span data-stu-id="74a10-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="74a10-111">La raison pour laquelle ces attributs sont définis, au lieu d’utiliser simplement une méthode pour toutes les propriétés MAPI de codage d’uniforme — consiste à autoriser la compatibilité descendante avec les logiciels non compatibles MAPI à l’aide de TNEF.</span><span class="sxs-lookup"><span data-stu-id="74a10-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="74a10-112">Le reste de cette section décrit la structure et la syntaxe d’un flux TNEF, le mappage entre les propriétés MAPI et attributs TNEF et considérations importantes pour certains attributs TNEF.</span><span class="sxs-lookup"><span data-stu-id="74a10-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  

