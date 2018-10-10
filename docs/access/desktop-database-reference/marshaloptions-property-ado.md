---
title: MarshalOptions, propriété (ADO)
TOCTitle: MarshalOptions Property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f290f2f4fb4820fb01d3a63aef7bcfbfa7c1f035
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471636"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique les enregistrements dont les paramètres doivent être convertis avant d'être renvoyés vers le serveur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs renvoyées

Définit ou renvoie une valeur [MarshalOptions](marshaloptionsenum.md). La valeur par défaut est **adMarshalAll**.

## <a name="remarks"></a>Remarques

Lorsque l'on utilise un [Recordset](recordset-object-ado.md) côté client, les enregistrements modifiés sur le client sont réécrits sur le niveau intermédiaire ou le serveur Web via une technique appelée marshaling ou conversion de paramètres (processus d'empaquetage et d'envoi des paramètres des méthodes de l'interface au-delà des limites des threads ou des processus). La définition de la propriété **MarshalOptions** peut améliorer les performances lorsque les paramètres des données distantes modifiées sont convertis pour être mis à jour sur le niveau intermédiaire ou le serveur Web.

**L’utilisation du Service de données à distance** Cette propriété est utilisée uniquement sur un **jeu d’enregistrements**du côté client.

