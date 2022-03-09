---
title: Convention d’attribution de noms de valeur de retour
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
ms.openlocfilehash: 347f4188b220ece15b15585d07d54ce6c725e423
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379051"
---
# <a name="return-value-naming-convention"></a>Convention d’attribution de noms de valeur de retour

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
The MAPICODE. Le fichier d’en-tête H contient de nombreuses valeurs qu’un client ou un fournisseur de services peut renvoyer à partir d’une implémentation de méthode d’interface ou qu’un appel peut renvoyer.
  
Les codes qui représentent des conditions d’avertissement et d’échec suivent une convention d’attribution de noms différente qui commence par le préfixe MAPI, un trait de soulignement et un W ou un E pour indiquer le type de code. Le reste du code est une courte chaîne de caractères pour décrire la condition. Chaque mot de la chaîne est séparé par un trait de soulignement. Par exemple, la valeur d’MAPI_E_TOO_COMPLEX indique que l’implémentation n’a pas pu gérer ce qui était demandé dans l’appel. La valeur d MAPI_W_PARTIAL_COMPLETION indique que l’appel a réussi, mais qu’il y a eu des problèmes. Seule une partie de l’opération a été effectuée avec succès.
  

