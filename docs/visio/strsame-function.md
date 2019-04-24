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
description: Détermine si les chaînes sont identiques. Elle renvoie TRUE si elles sont identiques et FALSe si elles ne le sont pas.
ms.openlocfilehash: 0f298c966ec7a3f1e23c89473fecc555ed950f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329840"
---
# <a name="strsame-function"></a>Fonction STRSAME

Détermine si les chaînes sont identiques. Elle renvoie TRUE si elles sont identiques et FALSe si elles ne le sont pas. 
  
## <a name="syntax"></a>Syntaxe

STRSAME ("* * *Chaîne1* * *", "* * *Chaîne2* * *", * * *ignoreCase* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |Obligatoire  <br/> |**String** <br/> |Première chaîne à comparer.  <br/> |
| _string2_ <br/> |Obligatoire  <br/> |**String** <br/> |Deuxième chaîne à comparer.  <br/> |
| _ignoreCase_ <br/> |Facultatif  <br/> |**Booléen** <br/> |Valeur TRUE pour ne pas tenir compte de la casse et valeur FALSE pour tenir compte de la casse dans la comparaison. La valeur par défaut est FALSE.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Booléen
  
## <a name="remarks"></a>Remarques

Pour comparer des chaînes multi-octets ou pour effectuer des comparaisons en utilisant les règles de casse pour un paramètre régional spécifique, utilisez la fonction STRSAMEEX.
  
## <a name="example-1"></a>Exemple 1

STRSAME ("cat", "Dog")
  
Renvoie la valeur FALSE.
  
## <a name="example-2"></a>Exemple 2

STRSAME ("cat", "cat")
  
Renvoie la valeur TRUE.
  
## <a name="example-3"></a>Exemple 3

STRSAME("chat","chat", TRUE)
  
Renvoie la valeur TRUE.
  
## <a name="example-4"></a>Exemple 4

STRSAME ("cat", "CAT")
  
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
  

