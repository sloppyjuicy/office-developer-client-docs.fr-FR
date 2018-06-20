---
title: Convention d’affectation de valeur de retour
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 990a48c661621a3a704236a850f5d09239a12fca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787029"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="a6a78-103">Convention d’affectation de valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a6a78-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="a6a78-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6a78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6a78-105">Le MAPICODE. Fichier d’en-tête H contient de nombreux les valeurs qu’un client ou fournisseur de services peut retourner à partir d’une implémentation de méthode d’interface ou peut voir renvoyé à partir d’un appel.</span><span class="sxs-lookup"><span data-stu-id="a6a78-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="a6a78-106">Les codes pour représenter l’avertissement et les défaillances suivent une convention d’affectation de noms différents qui commence par le préfixe MAPI, un trait de soulignement et un W ou E pour indiquer le type de code.</span><span class="sxs-lookup"><span data-stu-id="a6a78-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="a6a78-107">Le reste du code est une chaîne de caractères courte pour décrire la condition.</span><span class="sxs-lookup"><span data-stu-id="a6a78-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="a6a78-108">Chaque mot de la chaîne est séparée par un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="a6a78-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="a6a78-109">Par exemple, la valeur d’erreur MAPI_E_TOO_COMPLEX indique que l’implémentation n’a pu répondre tout ce qui a été demandé lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="a6a78-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="a6a78-110">La valeur d’avertissement MAPI_W_PARTIAL_COMPLETION se produit indique que l’appel a réussi, mais qu’il y avait des problèmes.</span><span class="sxs-lookup"><span data-stu-id="a6a78-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="a6a78-111">Seule une partie de l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a6a78-111">Only part of the operation was completed successfully.</span></span>
  

