---
title: Convention d'affectation de noms de la valeur renvoyée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279824"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="99926-103">Convention d'affectation de noms de la valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="99926-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="99926-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99926-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99926-105">MAPICODE. H contient un grand nombre de valeurs qu'un client ou un fournisseur de services peut renvoyer à partir d'une implémentation de méthode d'interface ou peut voir retourné à partir d'un appel.</span><span class="sxs-lookup"><span data-stu-id="99926-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="99926-106">Les codes permettant de représenter les conditions d'avertissement et d'échec suivent une convention d'affectation de noms différente qui commence par le préfixe MAPI, un trait de soulignement et un W ou un E pour indiquer le type de code.</span><span class="sxs-lookup"><span data-stu-id="99926-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="99926-107">Le reste du code est une chaîne de caractères courts pour décrire la condition.</span><span class="sxs-lookup"><span data-stu-id="99926-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="99926-108">Chaque mot de la chaîne est séparé par un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="99926-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="99926-109">Par exemple, la valeur d'erreur MAPI_E_TOO_COMPLEX indique que l'implémentation n'a pas pu gérer ce qui était demandé dans l'appel.</span><span class="sxs-lookup"><span data-stu-id="99926-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="99926-110">La valeur d'avertissement MAPI_W_PARTIAL_COMPLETION indique que l'appel a réussi, mais qu'il y a eu des problèmes.</span><span class="sxs-lookup"><span data-stu-id="99926-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="99926-111">Seule une partie de l'opération s'est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="99926-111">Only part of the operation was completed successfully.</span></span>
  

