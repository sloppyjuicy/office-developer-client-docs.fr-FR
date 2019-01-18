---
title: Propriété Recordset2.UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d655ba231466ac41902dba3a1422ca02893938f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698665"
---
# <a name="recordset2updateoptions-property-dao"></a>Propriété Recordset2.UpdateOptions (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . UpdateOptions (OptionsMAJ)

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Lorsqu'une méthode **[Update](recordset2-update-method-dao.md)** en mode de traitement par lot est exécutée, DAO et la bibliothèque client de curseurs par lots créent une série d'instructions SQL UPDATE pour apporter les modifications nécessaires. Une clause SQL WHERE est créée pour chaque mise à jour afin d'isoler les enregistrements marqués comme étant modifiés par la propriété **[RecordStatus](recordset2-recordstatus-property-dao.md)**. Dans la mesure où certains serveurs distants utilisent des déclencheurs ou d'autres moyens pour appliquer l'intégrité référentielle, il est souvent essentiel de limiter les champs à mettre à jour aux seuls champs affectés par la modification. 

Pour ce faire, affectez à la propriété **UpdateOptions** l'une des constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** ou **dbCriteriaTimeStamp**. De cette façon, seule la partie minimale indispensable du code de déclencheur est exécutée. Ainsi, l'opération de mise à jour est exécutée plus rapidement et est moins susceptible de contenir des erreurs.

h **dbCriteriaDeleteInsert** **dbCriteriaUpdate** **UpdateOptions**

Si vous ne spécifiez pas de constantes, **dbCriteriaUpdate** et **dbCriteriaKey** seront utilisées.

Dans la mesure où les enregistrements récemment ajoutés génèrent toujours des instructions INSERT et les enregistrements supprimés toujours des instructions DELETE, cette propriété ne concerne que la façon dont la bibliothèque de curseurs met à jour les enregistrements modifiés.

