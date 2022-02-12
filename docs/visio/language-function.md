---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permet d’établir des opérations de comparaison entre différentes représentations linguistiques. Il est préférable pour convertir des balises de langue BCP 47 (Internet Engineering Task Force) en valeurs d’ID de paramètres régionaux (LCID).
ms.openlocfilehash: 4ecbecd8222f1d4ba66d557b953a6dee5d6041f1
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771278"
---
# <a name="language-function"></a>LANGUAGE Function

Permet d’établir des opérations de comparaison entre différentes représentations linguistiques. Il est préférable pour convertir des balises de langue BCP 47 (Internet Engineering Task Force) en valeurs d’ID de paramètres régionaux (LCID).
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013
 
  
## <a name="syntax"></a>Syntaxe

 **LANGUAGE**( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Requis  <br/> |**String** <br/> |Valeur LCID ou BCP 47 pour la langue. |
   
## <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="example"></a>Exemple

 `LANGUAGE("en-us")`
  
Renvoie la valeur « 1033 ».
  
 `LANGUAGE("es-es")`
  
Renvoie la valeur « 3082 ».
  

