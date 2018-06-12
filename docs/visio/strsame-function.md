---
title: STRSAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: Détermine si les chaînes sont identiques. Elle renvoie la valeur TRUE si elles sont identiques et FALSE si elles ne sont pas.
ms.openlocfilehash: 5365ce6e679f708a47f4bcbdebbc4cabb13a2aee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789813"
---
# <a name="strsame-function"></a>STRSAME, fonction

Détermine si les chaînes sont identiques. Elle renvoie la valeur TRUE si elles sont identiques et FALSE si elles ne sont pas. 
  
## <a name="syntax"></a>Syntaxe

STRSAME (« ** *chaîne1* ** «, » ** *chaîne2* ** », ** *ignoreCase* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _chaîne string1_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Première chaîne à comparer.  <br/> |
| _chaîne2_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Deuxième chaîne à comparer.  <br/> |
| _ignoreCase_ <br/> |Facultatif  <br/> |**Boolean** <br/> |Valeur TRUE pour ne pas tenir compte de la casse et valeur FALSE pour tenir compte de la casse dans la comparaison. La valeur par défaut est FALSE.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Booléenne
  
## <a name="remarks"></a>Remarques

Pour comparer des chaînes multi-octets ou pour effectuer des comparaisons en utilisant les règles de casse pour un paramètre régional spécifique, utilisez la fonction STRSAMEEX.
  
## <a name="example-1"></a>Exemple 1

STRSAME("chat","chien")
  
Renvoie la valeur FALSE.
  
## <a name="example-2"></a>Exemple 2

STRSAME("chat","chat")
  
Renvoie la valeur TRUE.
  
## <a name="example-3"></a>Exemple 3

STRSAME("chat","chat", TRUE)
  
Renvoie la valeur TRUE.
  
## <a name="example-4"></a>Exemple 4

STRSAME("chat","CHAT")
  
Renvoie la valeur FALSE.
  
## <a name="example-5"></a>Exemple 5

STRSAME("chat","CHAT", TRUE)
  
Renvoie la valeur TRUE.
  
## <a name="example-6"></a>Exemple 6

STRSAME("chât","CHAT", TRUE)
  
Renvoie la valeur FALSE.
  
## <a name="example-7"></a>Exemple 7

STRSAME("chât","CHÂT", TRUE)
  
Renvoie la valeur TRUE.
  

