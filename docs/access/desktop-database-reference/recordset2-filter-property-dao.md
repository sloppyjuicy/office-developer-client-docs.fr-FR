---
title: Recordset2. Filter, propriété (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 19f3c017aa5d4a353f3e832a3678d921565ea822
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307328"
---
# <a name="recordset2filter-property-dao"></a>Recordset2. Filter, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui détermine les enregistrements inclus dans l'objet **Recordset** ouvert ultérieurement (espace de travail Microsoft Access uniquement. Valeur **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* . Éliminer

*expression* Expression qui renvoie un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est un type de données String qui contient une clause WHERE d'une instruction SQL sans le mot réservé WHERE.

Utilisez la propriété **Filter** pour appliquer un filtre à un objet **Recordset** de type feuille de réponse dynamique, instantané ou avant uniquement.

La propriété **Filter** permet de limiter le nombre d’enregistrements renvoyés à partir d’un objet existant lorsqu’un nouvel objet **Recordset** est ouvert sur la base d’un objet **Recordset** existant.

Utiliser le format de date américain (mois-jour-année) lorsque vous filtrez des champs contenant des dates, même si vous n'utilisez pas la version américaine du moteur de base de données Microsoft Access (auquel cas vous devez assembler n'importe quelle date en concaténant des chaînes, par exemple, strMonth & "-" _ aMP_ strDay & "-" & strYear). Sinon, il est possible que le filtrage des données ne donne pas les résultats escomptés.

Dans la plupart des cas, il est plus rapide d'ouvrir un nouvel objet **Recordset** à l'aide d'une instruction SQL qui comprend une clause WHERE.

Si vous affectez à la propriété une chaîne concaténée avec une valeur non entière et que les paramètres système spécifient un caractère non-U. S. Decimal tel qu'une virgule (par exemple, strFilter = " \> Price" & lngPrice et lngPrice = 125, 50), une erreur se produit lorsque vous essayez de ouvre le **jeu d'enregistrements**suivant. En effet, pendant la concaténation, le nombre est converti en une chaîne qui utilise le caractère décimal par défaut de votre système ; Microsoft Access SQL n'accepte que les caractères décimaux de l'anglais (États-Unis).

