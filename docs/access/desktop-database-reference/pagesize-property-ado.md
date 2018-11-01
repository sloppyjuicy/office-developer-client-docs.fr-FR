---
title: PageSize, propriété (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9b2a5857ef5d04bd45a36176d7daeebaf63678d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883273"
---
# <a name="pagesize-property-ado"></a>PageSize, propriété (ADO)


**S’applique à**: Access 2013, Office 2013

Indique combien d'enregistrements constituent une page dans le [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou retourne une valeur de type **Long** qui indique le nombre d'enregistrements sur une page. La valeur par défaut est 10.

## <a name="remarks"></a>Remarques

La propriété **PageSize** permet de déterminer le nombre d'enregistrements constituant une page logique de données. La définition d'une taille de page vous permet d'utiliser la propriété [AbsolutePage](absolutepage-property-ado.md) pour accéder au premier enregistrement d'une page donnée. Cela est utile dans les scénarios de serveur web lorsque vous souhaitez permettre à l’utilisateur de parcourir les données, consulter un certain nombre d’enregistrements à la fois.

Cette propriété peut être définie à tout moment ; sa valeur est utilisée pour calculer l'emplacement du premier enregistrement d'une page donnée.

