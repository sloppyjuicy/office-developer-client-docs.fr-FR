---
title: WEEKDAY Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
ms.localizationpriority: medium
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Renvoie un integer, de 1 à 7, qui représente le jour de la semaine dans l’heure ou l’expression.
ms.openlocfilehash: 8227def3922e68239c4b984ec29be0f94bfe78f6
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775202"
---
# <a name="weekday-function-visioshapesheet"></a>WEEKDAY Function (VisioShapeSheet)

Renvoie un integer, de 1 à 7, qui représente le jour de la semaine dans  _l’heure ou_  _l’expression_.
  
## <a name="syntax"></a>Syntaxe

WEEKDAY( » ** *datetime* ** « | ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Requis  <br/> |**String** <br/> | Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure. |
| _expression_ <br/> |Requis  <br/> |**Varie** <br/> |Toute expression qui génère une date et une heure. |
| _lcid_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système. |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Le composant d’heure  _dans l’heure ou_  _l’expression_ est ignoré. 
  
Le résultat est compris entre lundi (1) et dimanche (7). Aucun arrondissement n’est effectué. Si  _la date/_ heure est manquante ou ne peut pas être interprétée comme une date ou une heure valide, la fonction renvoie une #VALUE! erreur. 
  
La fonction WEEKDAY accepte également une valeur de nombre unique pour  _l’expression_ où la partie nombre inte du résultat représente le nombre de jours depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

WEEKDAY("30 mai 1999")
  
Renvoie 7.
  
## <a name="example-2"></a>Exemple 2

WEEKDAY(VALEURDATE("30 mai 1999") + 2 je.)
  
Renvoie 2.
  
## <a name="example-3"></a>Exemple 3

WEEKDAY(35880.6337)
  
Renvoie 4.
  

