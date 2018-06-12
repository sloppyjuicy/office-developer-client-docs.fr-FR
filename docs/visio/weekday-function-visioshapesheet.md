---
title: WEEKDAY, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Renvoie un entier, de 1 à 7, représentant le jour de datetime ou expression.
ms.openlocfilehash: decc89c93d175b357cdfe2b8377d04517b92ccab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790035"
---
# <a name="weekday-function-visioshapesheet"></a>WEEKDAY, fonction (VisioShapeSheet)

Renvoie un entier, de 1 à 7, représentant le jour de la semaine dans _datetime_ ou _expression_.
  
## <a name="syntax"></a>Syntaxe

WEEKDAY (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**Varie** <br/> |Toute expression qui génère une date et une heure.  <br/> |
| _LCID_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Entier
  
## <a name="remarks"></a>Remarques

Le composant heure de _datetime_ ou _expression_ est ignoré. 
  
Le résultat correspond au lundi (1) et dimanche (7). Aucun arrondi n’est effectué. Si _datetime_ est introuvable ou ne peut pas être interprété comme une date ou heure valide, la fonction retourne un #VALUE ! erreur. 
  
La fonction WEEKDAY accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

WEEKDAY("30 mai 1999")
  
Renvoie 7.
  
## <a name="example-2"></a>Exemple 2

WEEKDAY(VALEURDATE("30 mai 1999") + 2 je.)
  
Renvoie 2.
  
## <a name="example-3"></a>Exemple 3

WEEKDAY(35880.6337)
  
Renvoie 4.
  

