---
title: Positionnement du jeu d'enregistrements
TOCTitle: Recordset Positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10586c711b9931c1cac93401111f4d477ca8a987
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472201"
---
# <a name="recordset-positioning"></a>Positionnement du jeu d'enregistrements


**S’applique à**: Access 2013 | Office 2013

La propriété **AbsolutePosition** permet d'accéder à un enregistrement donné, en fonction de sa position ordinale dans l'objet **Recordset** ou de déterminer la position ordinale de l'enregistrement actif. Le fournisseur doit prendre en charge les fonctionnalités requises pour que cette propriété soit disponible.

**AbsolutePosition** utilise des nombres en base 1 et est égale à 1 lorsque l'enregistrement actif est le premier de l'objet **Recordset**. Comme nous l'avons mentionné, la propriété **RecordCount** permet de déterminer le nombre d'enregistrements de l'objet **Recordset**.

Lorsque vous définissez la propriété **AbsolutePosition**, même si elle s'applique à un enregistrement stocké dans le cache actuel, ADO recharge le cache avec un nouveau groupe d'enregistrements, en commençant par l'enregistrement spécifié. La propriété **CacheSize** détermine, quant à elle, la taille de ce groupe.


> [!NOTE]
> <P>[!REMARQUE] Vous ne pouvez pas utiliser la propriété <STRONG>AbsolutePosition</STRONG> en tant que numéro d'enregistrement de substitution. En effet, la position d'un enregistrement change lorsque vous supprimez l'enregistrement précédent et rien ne garantit que la valeur de la propriété <STRONG>AbsolutePosition</STRONG> restera identique si l'objet <STRONG>Recordset</STRONG> est rouvert ou fait l'objet d'une nouvelle requête. L'utilisation des signets est recommandée pour conserver ou revenir à une position donnée. En outre, ils constituent le seul moyen de se positionner dans tous les types d'objets <STRONG>Recordset</STRONG>.</P>


