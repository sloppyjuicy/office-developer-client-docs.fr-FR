---
title: PageSize, propriété (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 41a70c07939b979c632636352c5b0a642973b5e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562558"
---
# <a name="pagesize-property-ado"></a>PageSize, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique combien d’enregistrements constituent une page dans le [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou retourne une valeur de type **Long** qui indique le nombre d'enregistrements sur une page. La valeur par défaut est 10.

## <a name="remarks"></a>Remarques

La propriété **PageSize** permet de déterminer le nombre d'enregistrements constituant une page logique de données. La définition d'une taille de page vous permet d'utiliser la propriété [AbsolutePage](absolutepage-property-ado.md) pour accéder au premier enregistrement d'une page donnée. Cela est utile dans les scénarios de serveur web lorsque vous souhaitez autoriser l’utilisateur à paginer des données, en visualant un certain nombre d’enregistrements à la fois.

Cette propriété peut être définie à tout moment et sa valeur sera utilisée pour calculer l'emplacement du premier enregistrement d'une page donnée.

