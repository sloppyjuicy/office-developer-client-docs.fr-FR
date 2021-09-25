---
title: Recordset2.Filter, propriété (DAO)
TOCTitle: Filter Property
ms:assetid: 5b3b4e18-8af4-5acd-a129-513ba2d913d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194529(v=office.15)
ms:contentKeyID: 48545069
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053062
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 757aec47564e6462bf543e408825367ef26b775c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605980"
---
# <a name="recordset2filter-property-dao"></a>Recordset2.Filter, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui détermine les enregistrements inclus dans l'objet **Recordset** ouvert ultérieurement (espace de travail Microsoft Access uniquement. Type **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* .Filter

*expression* Expression qui renvoie un **objet Recordset2.**

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est un type de données String qui contient une clause WHERE d'une instruction SQL sans le mot réservé WHERE.

Utilisez la propriété **Filter** pour appliquer un filtre à un objet **Recordset** de type feuille de réponse dynamique, instantané ou avant uniquement.

La propriété **Filter** permet de limiter le nombre d’enregistrements renvoyés à partir d’un objet existant lorsqu’un nouvel objet **Recordset** est ouvert sur la base d’un objet **Recordset** existant.

Utilisez le format de date américain (mois-jour-année) lorsque vous filtrez des champs contenant des dates, même si vous ne disposez pas de la version américaine du moteur de base de données Microsoft Access (dans ce cas, vous devez assembler les dates en concaténant des chaînes, par exemple strMonth & "-" & strDay & "-" & strYear). Sinon, il est possible que le filtrage des données ne donne pas les résultats escomptés.

Dans la plupart des cas, il est plus rapide d’ouvrir un nouvel objet **Recordset** à l’aide d’une instruction SQL qui inclut une clause WHERE.

Si vous affectez à la propriété une chaîne concaténée avec une valeur non entière et que les paramètres système spécifient un caractère décimal américain tel que la virgule (par exemple, strFilter = "PRICE \> " & lngPrice et lngPrice = 125,50), une erreur est générée lorsque vous tentez d'ouvrir l'objet **Recordset** suivant. En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.

