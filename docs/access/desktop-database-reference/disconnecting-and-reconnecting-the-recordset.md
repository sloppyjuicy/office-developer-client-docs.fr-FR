---
title: Déconnexion et reconnexion de l’objet Recordset
TOCTitle: Disconnecting and reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac1bc4c9c9d6d149faeb18d73f17539e63a4147e
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943940"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a>Déconnexion et reconnexion de l’objet Recordset


**S’applique à**: Access 2013, Office 2013

## <a name="disconnecting-and-reconnecting-the-recordset"></a>Déconnexion et reconnexion du recordset

Une des fonctionnalités les plus puissantes d'ADO permet d'ouvrir un objet **Recordset** côté client à partir d'une source de données et de *déconnecter* cet objet **Recordset** de la source de données. Après la déconnexion de l'objet **Recordset**, la connexion à la source de données peut être fermée, libérant ainsi les ressources serveur utilisées pour la gérer. Vous pouvez continuer à consulter et modifier les données dans l'objet **Recordset** pendant sa déconnexion puis le reconnecter ultérieurement à la source de données et envoyer vos mises à jour en mode de mise à jour par lot.

Pour déconnecter un objet **Recordset**, ouvrez-le avec un emplacement de curseur dont la valeur est **adUseClient** puis affectez à la propriété **ActiveConnection** la valeur *Nothing*. (Les utilisateurs de C++ doivent affecter la valeur NULL à **ActiveConnection** pour effectuer une déconnexion.)

Nous aurons recours à un objet **Recordset** déconnecté plus loin dans ce chapitre, lorsque nous aborderons la persistance de l'objet **Recordset**. Il sera utilisé pour illustrer un scénario dans lequel les données de l'objet **Recordset** doivent être mises à la disposition d'une application lorsque l'ordinateur client n'est pas connecté à un réseau.

