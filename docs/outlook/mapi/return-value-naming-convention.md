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
# <a name="return-value-naming-convention"></a>Convention d’affectation de valeur de retour

  
  
**S’applique à**: Outlook 
  
Le MAPICODE. Fichier d’en-tête H contient de nombreux les valeurs qu’un client ou fournisseur de services peut retourner à partir d’une implémentation de méthode d’interface ou peut voir renvoyé à partir d’un appel.
  
Les codes pour représenter l’avertissement et les défaillances suivent une convention d’affectation de noms différents qui commence par le préfixe MAPI, un trait de soulignement et un W ou E pour indiquer le type de code. Le reste du code est une chaîne de caractères courte pour décrire la condition. Chaque mot de la chaîne est séparée par un trait de soulignement. Par exemple, la valeur d’erreur MAPI_E_TOO_COMPLEX indique que l’implémentation n’a pu répondre tout ce qui a été demandé lors de l’appel. La valeur d’avertissement MAPI_W_PARTIAL_COMPLETION se produit indique que l’appel a réussi, mais qu’il y avait des problèmes. Seule une partie de l’opération a réussi.
  

