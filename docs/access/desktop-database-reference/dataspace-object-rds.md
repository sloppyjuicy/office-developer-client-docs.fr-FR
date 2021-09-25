---
title: Objet DataSpace (RDS)
TOCTitle: DataSpace object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b5a5aa610483a59976461b6efada64fa4208f31a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615619"
---
# <a name="dataspace-object-rds"></a>Objet DataSpace (RDS)

**S’applique à** : Access 2013, Office 2013

Crée des proxys côté client pour les objets métier personnalisés de la couche intermédiaire.

## <a name="remarks"></a>Remarques

Remote Data Service nécessite des proxys d'objets métier pour que le composant côté client puisse communiquer avec des objets métier situés au niveau intermédiaire. Les proxys permettent l'assemblage, le désassemblage et le transport (marshaling) des données de [Recordset](recordset-object-ado.md) d'une application pour qu'elles puissent franchir les frontières des processus et des machines.

Remote Data Service utilise la méthode **CreateObject** de l'objet [RDS.DataSpace](createobject-method-rds.md) pour créer des proxys d'objet métier. Un proxy d'objet métier est créé de manière dynamique chaque fois qu'une instance de son objet métier équivalent de niveau intermédiaire est créée. Remote Data Service prend en charge les protocoles suivants : HTTP, HTTPS (HTTP Secure Sockets), DCOM et in-process (les composants clients et l'objet métier résident sur le même ordinateur).

> [!NOTE]
> [!REMARQUE] RDS fonctionne « sans état » lorsque l'objet **RDS.DataSpace** utilise les protocoles HTTP ou HTTPS. En d'autres termes, toute information interne concernant une demande client est ignorée après le renvoi d'une réponse par le serveur.

Bien que l'objet métier semble exister pendant la durée du vie du proxy d'objet métier, il n'existe en fait que jusqu'à ce qu'une réponse à la demande soit envoyée. Lorsqu'une demande est émise (quand une méthode est appelée pour l'objet métier), le proxy ouvre une nouvelle connexion sur le serveur et ce dernier crée une nouvelle instance de l'objet métier. Lorsque ce dernier a répondu à la demande, le serveur le détruit et ferme la connexion.

Ce comportement signifie que vous ne pouvez pas passer de données d'une demande à une autre à l'aide d'une propriété ou d'une variable de l'objet métier. Vous devez utiliser un autre mécanisme, comme un fichier ou un argument de méthode, pour rendre persistantes les données d'état.

L'identificateur de classe (Class ID) de l'objet **RDS.DataControl** est BD96C556-65A3-11D0-983A-00C04FC29E36.

