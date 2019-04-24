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
# <a name="return-value-naming-convention"></a>Convention d'affectation de noms de la valeur renvoyée

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPICODE. H contient un grand nombre de valeurs qu'un client ou un fournisseur de services peut renvoyer à partir d'une implémentation de méthode d'interface ou peut voir retourné à partir d'un appel.
  
Les codes permettant de représenter les conditions d'avertissement et d'échec suivent une convention d'affectation de noms différente qui commence par le préfixe MAPI, un trait de soulignement et un W ou un E pour indiquer le type de code. Le reste du code est une chaîne de caractères courts pour décrire la condition. Chaque mot de la chaîne est séparé par un trait de soulignement. Par exemple, la valeur d'erreur MAPI_E_TOO_COMPLEX indique que l'implémentation n'a pas pu gérer ce qui était demandé dans l'appel. La valeur d'avertissement MAPI_W_PARTIAL_COMPLETION indique que l'appel a réussi, mais qu'il y a eu des problèmes. Seule une partie de l'opération s'est terminée avec succès.
  

