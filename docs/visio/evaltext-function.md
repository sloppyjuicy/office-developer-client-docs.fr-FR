---
title: EVALTEXT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Évalue le texte dans l’argument shapename comme s’il a été une formule et renvoie le résultat.
ms.openlocfilehash: 69e79a23faa9d09aa2ad51f83363064b54742152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788573"
---
# <a name="evaltext-function"></a>EVALTEXT, fonction

Évalue le texte dans _l’argument shapename_ comme s’il a été une formule et renvoie le résultat. 
  
## <a name="syntax"></a>Syntaxe

EVALTEXT (** *shapename ! theText* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _l’argument shapename ! theText_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Cellule générée lorsque la composition du texte de la forme associée est modifiée.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

 _l’argument shapename_ peut servir à faire référence au texte d’une forme autre que la forme active. 
  
En l’absence de texte, le résultat est zéro. Si le texte ne peut pas être calculé, la fonction renvoie une erreur.
  
## <a name="example"></a>Exemple

EVALTEXT(Line.2!TheText) 
  
Évalue le texte contenu dans la forme Trait.2. Si, par exemple, Trait.2 contient « 121,92 cm + 15,24 cm », la valeur 137,16 cm est renvoyée. 
  

