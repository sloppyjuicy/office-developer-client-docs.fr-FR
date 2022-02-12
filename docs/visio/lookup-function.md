---
title: LOOKUP, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251457
ms.localizationpriority: medium
ms.assetid: cb6ec664-6062-75d0-1514-8058b98c2c36
description: Renvoie un index de base zéro qui indique l’emplacement de la clé de sous-chaîne dans une liste, ou renvoie -1 si la chaîne cible contient le délimiteur.
ms.openlocfilehash: 7396b6baef9ed19377c4b54861a29a57b8bca984
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771222"
---
# <a name="lookup-function"></a>Fonction LOOKUP

Renvoie un index de base zéro qui indique l’emplacement de la clé de sous-chaîne dans une _liste, ou_ renvoie -1 si la chaîne cible contient  le _délimiteur_.
  
## <a name="syntax"></a>Syntaxe

LOOKUP( » ** *key* ** « , » ** *list* ** « [, » ** *delimiter* ** « ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _key_ <br/> |Requis  <br/> |**String** <br/> |Chaîne à rechercher |
| _list_ <br/> |Requis  <br/> |**String** <br/> | Liste dans laquelle effectuer la recherche. |
| _delimiter_ <br/> |Facultatif  <br/> |**Chaîne** <br/> | Chaîne à utiliser comme délimiteur dans la  _liste_. Une  _chaîne de délimiteur_ peut comporter plusieurs caractères et inclure des caractères multioctets. La valeur par défaut est le point-virgule. |
   
### <a name="return-value"></a>Valeur renvoyée

Numérique
  
## <a name="remarks"></a>Remarques

La fonction LOOKUP ne tient pas compte des majuscules ou des minuscules. Si la liste commence ou finit par un délimiteur, on considère qu’une chaîne nulle est placée avant ou après la liste. Si plusieurs délimiteurs se suivent, on considère qu’ils sont séparés par une chaîne nulle. 
  
Tous les arguments doivent être des chaînes ou des expressions qui peuvent être convertis en chaînes. Si la conversion est impossible, une chaîne vide vient remplacer l’argument non accepté. 
  
## <a name="example-1"></a>Exemple 1

LOOKUP(« rat »,"cat;rat;; ; ]
  
Renvoie 1.
  
## <a name="example-2"></a>Exemple 2

LOOKUP(«  », »;cat;rat;; ; ]
  
Renvoie 0.
  
## <a name="example-3"></a>Exemple 3

LOOKUP(« t »,"cat;rat;; ; « "a »)
  
Renvoie 3.
  

