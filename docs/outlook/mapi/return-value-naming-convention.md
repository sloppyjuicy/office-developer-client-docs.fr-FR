---
title: Convention d’affectation de noms de valeur renvoyée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4d7a95e4681370e1aaf4f8b4c4b7ca0814b3aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581845"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="50386-103">Convention d’affectation de noms de valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="50386-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="50386-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50386-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50386-105">Le MAPICODE. Fichier d’en-tête H contient de nombreux les valeurs qu’un client ou fournisseur de services peut retourner à partir d’une implémentation de méthode d’interface ou peut voir renvoyé à partir d’un appel.</span><span class="sxs-lookup"><span data-stu-id="50386-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="50386-106">Les codes pour représenter l’avertissement et les défaillances suivent une convention d’affectation de noms différents qui commence par le préfixe MAPI, un trait de soulignement et un W ou E pour indiquer le type de code.</span><span class="sxs-lookup"><span data-stu-id="50386-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="50386-107">Le reste du code est une chaîne de caractères courte pour décrire la condition.</span><span class="sxs-lookup"><span data-stu-id="50386-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="50386-108">Chaque mot de la chaîne est séparée par un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="50386-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="50386-109">Par exemple, la valeur d’erreur MAPI_E_TOO_COMPLEX indique que l’implémentation n’a pu répondre tout ce qui a été demandé lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="50386-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="50386-110">La valeur d’avertissement MAPI_W_PARTIAL_COMPLETION se produit indique que l’appel a réussi, mais qu’il y avait des problèmes.</span><span class="sxs-lookup"><span data-stu-id="50386-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="50386-111">Seule une partie de l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="50386-111">Only part of the operation was completed successfully.</span></span>
  

