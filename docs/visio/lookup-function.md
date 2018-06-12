---
title: LOOKUP, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251457
localization_priority: Normal
ms.assetid: cb6ec664-6062-75d0-1514-8058b98c2c36
description: Renvoie un index de base zéro qui indique l’emplacement de la sous-chaîne clé dans une liste ou renvoie -1 si la chaîne cible contient le séparateur.
ms.openlocfilehash: e1fd433282871135d385d1c980c77041cd49cdf4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789046"
---
# <a name="lookup-function"></a>LOOKUP, fonction

Renvoie un index de base zéro qui indique l’emplacement de la sous-chaîne _clé_ dans une _liste_ou renvoie -1 si la chaîne cible contient le _séparateur_.
  
## <a name="syntax"></a>Syntaxe

RECHERCHE (« ** *clé* ** », » ** *liste* ** « [, » ** *délimiteur* ** »]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _clé_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Chaîne à rechercher  <br/> |
| _liste_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Liste dans laquelle effectuer la recherche.  <br/> |
| _delimiter_ <br/> |Facultatif  <br/> |**Chaîne** <br/> | La chaîne à utiliser comme délimiteur dans la _liste_. Une chaîne de _délimiteur_ peut être plusieurs caractères et peut inclure des caractères codés. La valeur par défaut est un point-virgule.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Numérique
  
## <a name="remarks"></a>Note

La fonction LOOKUP ne tient pas compte des majuscules ou des minuscules. Si la liste commence ou finit par un délimiteur, on considère qu’une chaîne nulle est placée avant ou après la liste. Si plusieurs délimiteurs se suivent, on considère qu’ils sont séparés par une chaîne nulle. 
  
Tous les arguments doivent être des chaînes ou des expressions qui peuvent être convertis en chaînes. Si la conversion est impossible, une chaîne vide vient remplacer l’argument non accepté. 
  
## <a name="example-1"></a>Exemple 1

LOOKUP("rat","chat;rat;;chèvre")
  
Renvoie 1.
  
## <a name="example-2"></a>Exemple 2

LOOKUP("",";chat;rat;;chèvre")
  
Renvoie 0.
  
## <a name="example-3"></a>Exemple 3

LOOKUP("t","chat;rat;;chèvre","a")
  
Renvoie 3.
  

