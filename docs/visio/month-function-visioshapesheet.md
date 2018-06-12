---
title: MONTH, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Renvoie un entier compris entre 1 et 12 qui représente un mois.
ms.openlocfilehash: e17803a153b4aadec34aa751da7efa077963bba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789154"
---
# <a name="month-function-visioshapesheet"></a>MONTH, fonction (VisioShapeSheet)

Renvoie un entier compris entre 1 et 12 qui représente un mois.
  
## <a name="syntax"></a>Syntaxe

MOIS (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Toute expression qui génère une date et une heure.  <br/> |
| _LCID_ <br/> |Facultatif  <br/> |**Number** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Entier
  
## <a name="remarks"></a>Remarques

Le composant heure de _datetime_ ou _expression_ est ignoré. 
  
Aucun arrondissement n’est effectué. Si la chaîne d’entrée est introuvable ou ne peut pas être convertie en un résultat valide, la fonction MONTH renvoie une erreur.
  
La valeur renvoyée est formatée selon le format de date abrégée défini dans les paramètres régionaux actuels de votre système d’exploitation.
  
La fonction MONTH accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

MONTH("30 mai 1999 13:45:24")
  
Renvoie 5.
  
## <a name="example-2"></a>Exemple 2

MONTH(VALEURDATE("30 mai 1999") + 7 je.)
  
Renvoie 6.
  
## <a name="example-3"></a>Exemple 3

MONTH(35580.6337)
  
Renvoie 5.
  

