---
title: HOUR, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Renvoie un entier, 0 et 23 représentant l’heure du jour de datetime ou expression.
ms.openlocfilehash: 9cfe8c88a4a4d73be23b2ac230b0cfabc955c004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788785"
---
# <a name="hour-function-visioshapesheet"></a>HOUR, fonction (VisioShapeSheet)

Renvoie un entier, 0 et 23 représentant l’heure du jour de _datetime_ ou _expression_.
  
## <a name="syntax"></a>Syntaxe

HEURE (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**Varie** <br/> |Expression qui génère une date et une heure.  <br/> |
| _LCID_ <br/> |Facultatif  <br/> |**Number** <br/> | Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
## <a name="remarks"></a>Note

Le composant date de *datetime* et *expression* est ignoré. 
  
Aucun arrondi n’est effectué. Si *datetime* est introuvable ou ne peut pas être converti en un résultat valide, la fonction renvoie une erreur. 
  
La valeur renvoyée est formatée selon le format horaire défini dans les paramètres régionaux actuels de votre système d’exploitation. 
  
La fonction HOUR accepte également une valeur numérique simple pour *expression* où la partie décimale du résultat représente la fraction du jour depuis minuit. 
  
## <a name="example-1"></a>Exemple 1

HOUR("15:45:00")
  
Renvoie 15.
  
## <a name="example-2"></a>Exemple 2

HOUR("30 mai 1997 15:45:24")
  
Renvoie 15.
  
## <a name="example-3"></a>Exemple 3

HOUR(0.5)
  
Renvoie 12.
  
## <a name="example-4"></a>Exemple 4

HOUR("30/05/1997")
  
Renvoie 0.
  

