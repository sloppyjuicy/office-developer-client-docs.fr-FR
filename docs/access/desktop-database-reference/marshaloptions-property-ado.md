---
title: MarshalOptions, propriété (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704594"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions, propriété (ADO)


**S’applique à**: Access 2013, Office 2013

Indique les enregistrements dont les paramètres doivent être convertis avant d'être renvoyés vers le serveur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs renvoyées

Définit ou renvoie une valeur [MarshalOptions](marshaloptionsenum.md). La valeur par défaut est **adMarshalAll**.

## <a name="remarks"></a>Remarques

Lorsque vous utilisez un [jeu d’enregistrements](recordset-object-ado.md)du côté client, les enregistrements qui ont été modifiés sur le client sont réécrits au niveau intermédiaire ou au serveur web via une technique appelée marshaling, le processus d’empaquetage et d’envoi des paramètres de méthode d’interface entre les threads ou limites de processus. Définition de la propriété **MarshalOptions** peut améliorer les performances lors du marshaling de données distantes modifiées pour mettre à jour au niveau intermédiaire ou au serveur web.

**L’utilisation du Service de données à distance** Cette propriété est utilisée uniquement sur un **jeu d’enregistrements**du côté client.

