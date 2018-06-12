---
title: YEAR, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Renvoie un entier représentant l’année grégorien de datetime ou expression, la mise en forme selon le style de format de date abrégée défini par les paramètres de langue et de région actuelles du système.
ms.openlocfilehash: aaa183730440857d8d283912f4afeb3117ef737f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790092"
---
# <a name="year-function-visioshapesheet"></a>YEAR, fonction (VisioShapeSheet)

Renvoie un entier représentant l’année grégorien dans _datetime_ ou _expression de_mise en forme selon le style de format de date abrégée défini par les paramètres de langue et de région actuelles du système.
  
## <a name="syntax"></a>Syntaxe

ANNÉE (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **]) 
  
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
  
Aucun arrondi n’est effectué. Si _datetime_ est introuvable ou ne peut pas être interprété comme une date valide ou une heure, année renvoie une erreur. 
  
La fonction YEAR accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

YEAR("27/10/2007 13:45:24 PM")
  
Renvoie 2007.
  
## <a name="example-2"></a>Exemple 2

YEAR(VALEURDATE("25 déc. 2006") + 7 je.)
  
Renvoie 2007.
  
## <a name="example-3"></a>Exemple 3

YEAR(35580.6337)
  
Renvoie 1997.
  

