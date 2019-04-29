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
description: Renvoie un index de base zéro qui indique l'emplacement de la clé de sous-chaîne dans une liste ou renvoie-1 si la chaîne cible contient le délimiteur.
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410328"
---
# <a name="lookup-function"></a>Fonction LOOKUP

Renvoie un index de base zéro qui indique l'emplacement de la _clé_ de sous-chaîne dans une _liste_ou renvoie-1 si la chaîne cible contient __ le délimiteur.
  
## <a name="syntax"></a>Syntaxe

Lookup ("* * *Key* * *", "* * *List* * *" [, "* * ** délimiteur * *"]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _key_ <br/> |Obligatoire  <br/> |**String** <br/> |Chaîne à rechercher  <br/> |
| _liste_ <br/> |Obligatoire  <br/> |**String** <br/> | Liste dans laquelle effectuer la recherche.  <br/> |
| _delimiter_ <br/> |Facultatif  <br/> |**Chaîne** <br/> | Chaîne à utiliser en tant que délimiteur dans la _liste_. Une __ chaîne de délimiteur peut contenir plusieurs caractères et peut inclure des caractères multioctets. La valeur par défaut est le point-virgule.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Numérique
  
## <a name="remarks"></a>Remarques

La fonction LOOKUP ne tient pas compte des majuscules ou des minuscules. Si la liste commence ou finit par un délimiteur, on considère qu’une chaîne nulle est placée avant ou après la liste. Si plusieurs délimiteurs se suivent, on considère qu’ils sont séparés par une chaîne nulle. 
  
Tous les arguments doivent être des chaînes ou des expressions qui peuvent être convertis en chaînes. Si la conversion est impossible, une chaîne vide vient remplacer l’argument non accepté. 
  
## <a name="example-1"></a>Exemple 1

LOOKUP ("rat", "cat; rat;; chèvre ")
  
Renvoie 1.
  
## <a name="example-2"></a>Exemple 2

LOOKUP ("", "; cat; rat;; chèvre ")
  
Renvoie 0.
  
## <a name="example-3"></a>Exemple 3

LOOKUP ("t", "cat; rat;; chèvre "," a ")
  
Renvoie 3.
  

