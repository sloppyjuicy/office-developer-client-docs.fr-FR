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
# <a name="return-value-naming-convention"></a>Convention d’affectation de noms de valeur renvoyée

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le MAPICODE. Fichier d’en-tête H contient de nombreux les valeurs qu’un client ou fournisseur de services peut retourner à partir d’une implémentation de méthode d’interface ou peut voir renvoyé à partir d’un appel.
  
Les codes pour représenter l’avertissement et les défaillances suivent une convention d’affectation de noms différents qui commence par le préfixe MAPI, un trait de soulignement et un W ou E pour indiquer le type de code. Le reste du code est une chaîne de caractères courte pour décrire la condition. Chaque mot de la chaîne est séparée par un trait de soulignement. Par exemple, la valeur d’erreur MAPI_E_TOO_COMPLEX indique que l’implémentation n’a pu répondre tout ce qui a été demandé lors de l’appel. La valeur d’avertissement MAPI_W_PARTIAL_COMPLETION se produit indique que l’appel a réussi, mais qu’il y avait des problèmes. Seule une partie de l’opération a réussi.
  

