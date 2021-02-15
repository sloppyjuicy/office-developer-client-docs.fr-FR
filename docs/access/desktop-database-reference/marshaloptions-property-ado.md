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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289769"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique les enregistrements dont les paramètres doivent être convertis avant d'être renvoyés vers le serveur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs renvoyées

Définit ou renvoie une valeur [MarshalOptions](marshaloptionsenum.md). La valeur par défaut est **adMarshalAll**.

## <a name="remarks"></a>Remarques

Lors de l’utilisation d’un jeu d’enregistrements côté [client,](recordset-object-ado.md)les enregistrements qui ont été modifiés sur le client sont écrits sur le niveau intermédiaire ou le serveur web via une technique appelée marshaling, le processus d’empaquetage et l’envoi de paramètres de méthode d’interface au-delà des limites de thread ou de processus. La définition **de la propriété MarshalOptions** peut améliorer les performances lorsque les données distantes modifiées sont marshalées pour une mise à jour vers le niveau intermédiaire ou le serveur web.

**Utilisation du service de données à distance** Cette propriété est utilisée uniquement sur un **recordset** côté client.

