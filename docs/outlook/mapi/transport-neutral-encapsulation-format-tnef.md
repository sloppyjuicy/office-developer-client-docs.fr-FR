---
title: Format TNEF (Transport Neutral Encapsulation Format)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: Dernière modification le 12 mars 2013
ms.openlocfilehash: d902039fa1081e30947ddd8f70ead9ae7acec06a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356629"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="72ff2-103">Format TNEF (Transport Neutral Encapsulation Format)</span><span class="sxs-lookup"><span data-stu-id="72ff2-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="72ff2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72ff2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72ff2-105">Le format TNEF est un format permettant de convertir un ensemble de propriétés MAPI (un message MAPI) en un flux de données série.</span><span class="sxs-lookup"><span data-stu-id="72ff2-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="72ff2-106">Les fonctions TNEF sont principalement utilisées par les fournisseurs de transport qui doivent coder les propriétés de message MAPI pour la transmission via un système de messagerie qui ne prend pas directement en charge ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="72ff2-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="72ff2-107">Par exemple, un transport SMTP utilise le format TNEF pour coder les propriétés comme **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), qui n'ont pas de représentation directe dans la structure d'un message SMTP.</span><span class="sxs-lookup"><span data-stu-id="72ff2-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="72ff2-108">L'implémentation TNEF définit plusieurs attributs spécifiques au format TNEF, chacun correspondant à une propriété MAPI particulière.</span><span class="sxs-lookup"><span data-stu-id="72ff2-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="72ff2-109">Ces attributs sont utilisés pour encoder leurs propriétés MAPI respectives dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="72ff2-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="72ff2-110">De plus, un attribut spécial est défini qui peut être utilisé pour encapsuler une propriété MAPI qui n'a pas d'attribut spécifique correspondant.</span><span class="sxs-lookup"><span data-stu-id="72ff2-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="72ff2-111">La raison pour laquelle ces attributs sont définis, au lieu d'utiliser simplement une méthode de codage uniforme pour toutes les propriétés MAPI, est d'activer la compatibilité descendante avec un logiciel non conforme à la norme MAPI qui utilise le format TNEF.</span><span class="sxs-lookup"><span data-stu-id="72ff2-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="72ff2-112">Le reste de cette section décrit la structure et la syntaxe d'un flux TNEF, le mappage entre les propriétés MAPI et les attributs TNEF, ainsi que des considérations importantes pour certains attributs TNEF.</span><span class="sxs-lookup"><span data-stu-id="72ff2-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  

