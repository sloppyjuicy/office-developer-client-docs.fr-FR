---
title: PageSize, propriété (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9365acb13820f898c053d4c90fc252bfd3b228c4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709550"
---
# <a name="pagesize-property-ado"></a>PageSize, propriété (ADO)


**S’applique à**: Access 2013, Office 2013

Indique combien d'enregistrements constituent une page dans le [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou retourne une valeur de type **Long** qui indique le nombre d'enregistrements sur une page. La valeur par défaut est 10.

## <a name="remarks"></a>Remarques

La propriété **PageSize** permet de déterminer le nombre d'enregistrements constituant une page logique de données. La définition d'une taille de page vous permet d'utiliser la propriété [AbsolutePage](absolutepage-property-ado.md) pour accéder au premier enregistrement d'une page donnée. Cela est utile dans les scénarios de serveur web lorsque vous souhaitez permettre à l’utilisateur de parcourir les données, consulter un certain nombre d’enregistrements à la fois.

Cette propriété peut être définie à tout moment ; sa valeur est utilisée pour calculer l'emplacement du premier enregistrement d'une page donnée.

