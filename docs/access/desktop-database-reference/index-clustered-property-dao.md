---
title: Index.Clustered Property (DAO)
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
ms.openlocfilehash: 4cb0c51f454e4792a64fc55416464373ac667dcf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469372"
---
# <a name="indexclustered-property-dao"></a>Index.Clustered Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Définit ou renvoie une valeur qui indique si un objet **Index** représente un index cluster pour une table (espaces de travail Microsoft Access uniquement). Valeur de type **Boolean** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* . En cluster

*expression* Expression qui renvoie un objet **Index** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur renvoyée est un type de données booléen qui correspond à **True** si l'objet **Index** représente un index cluster.

Certains formats de base de données de bureau IISAM utilisent les index cluster. Un index cluster est constitué d'un ou plusieurs champs qui organisent ensemble tous les enregistrements d'une table dans un ordre prédéfini. Il permet d'accéder facilement aux enregistrements d'une table dans laquelle les valeurs d'index ne peuvent pas être uniques.

La propriété **Clustered** est en lecture/écriture pour un nouvel objet **Index** qui n'a pas encore été ajouté à une collection et en lecture seule pour un objet **Index** existant d'une collection **Indexes**.


> [!NOTE]
> <UL>
> <LI>
> <P>Les bases de données du moteur de base de données Microsoft Access ignorent la propriété <STRONG>Clustered</STRONG> car ce moteur ne prend pas en charge les index cluster.</P>
> <LI>
> <P>En ce qui concerne les sources de données ODBC, la propriété <STRONG>Clustered</STRONG> renvoie toujours la valeur <STRONG>False</STRONG>. Elle ne détecte pas si la source de données ODBC possède un index cluster.</P></LI></UL>


