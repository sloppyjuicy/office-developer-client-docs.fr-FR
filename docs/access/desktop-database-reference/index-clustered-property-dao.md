---
title: Index.Clustered, propriété (DAO)
TOCTitle: Clustered Property
ms:assetid: dd0876a9-b7fe-c8c8-e675-5ed758ce5bd3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835375(v=office.15)
ms:contentKeyID: 48548149
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052930
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 5ef312233b77170f0f6b42c9aa8e133ff4851ab3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626406"
---
# <a name="indexclustered-property-dao"></a>Index.Clustered, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique si un objet **Index** représente un index cluster pour une table (espaces de travail Microsoft Access uniquement). Valeur de type **Boolean** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*.* Clustered

*expression* Expression qui renvoie un objet **Index.**

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur renvoyée est un type de données booléen qui correspond à **True** si l'objet **Index** représente un index cluster.

Certains formats de base de données de bureau IISAM utilisent les index cluster. Un index cluster est constitué d'un ou plusieurs champs qui organisent ensemble tous les enregistrements d'une table dans un ordre prédéfini. Il permet d'accéder facilement aux enregistrements d'une table dans laquelle les valeurs d'index ne peuvent pas être uniques.

La propriété **Clustered** est en lecture/écriture pour un nouvel objet **Index** qui n'a pas encore été ajouté à une collection et en lecture seule pour un objet **Index** existant d'une collection **Indexes**.

> [!NOTE]
> - Les bases de données du moteur de base de données Microsoft Access ignorent la propriété **Clustered** car ce moteur ne prend pas en charge les index cluster.
> - Pour les sources de données ODBC, la **propriété Clustered** renvoie toujours **la valeur False**; Il ne détecte pas si la source de données ODBC possède un index en cluster.


