---
title: Convention d’attribution de noms de valeur de retour
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423614"
---
# <a name="return-value-naming-convention"></a>Convention d’attribution de noms de valeur de retour

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
The MAPICODE. Le fichier d’en-tête H contient de nombreuses valeurs qu’un client ou un fournisseur de services peut renvoyer à partir d’une implémentation de méthode d’interface ou qu’un appel peut renvoyer.
  
Les codes qui représentent des conditions d’avertissement et d’échec suivent une convention d’attribution de noms différente qui commence par le préfixe MAPI, un trait de soulignement et un W ou un E pour indiquer le type de code. Le reste du code est une courte chaîne de caractères pour décrire la condition. Chaque mot de la chaîne est séparé par un trait de soulignement. Par exemple, la valeur d’MAPI_E_TOO_COMPLEX indique que l’implémentation n’a pas pu gérer ce qui était demandé dans l’appel. La valeur d MAPI_W_PARTIAL_COMPLETION indique que l’appel a réussi, mais qu’il y a eu des problèmes. Seule une partie de l’opération a été effectuée avec succès.
  

