---
title: Modèle de programmation RDS en détail
TOCTitle: RDS programming model in detail
ms:assetid: 133fc059-9b51-52e2-2e61-339716d8d965
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248906(v=office.15)
ms:contentKeyID: 48543364
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a3144f3f981d42868dfe2841ba9fd93dbb73c564
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597036"
---
# <a name="rds-programming-model-in-detail"></a>Modèle de programmation RDS en détail

**S’applique à** : Access 2013, Office 2013

La liste ci-dessous répertorie les éléments-clés du modèle de programmation RDS :

- RDS. DataSpace
- RDSServer.DataFactory
- RDS. DataControl
- Événements

## <a name="rdsdataspace"></a>RDS. DataSpace

Votre application cliente doit spécifier le serveur et le programme serveur à appeler. En retour, votre application reçoit une référence au programme serveur et est en mesure de traiter la référence comme s'il s'agissait du programme serveur lui-même.

Le modèle objet RDS fournit cette fonctionnalité grâce à l'objet [RDS.DataSpace](dataspace-object-rds.md).

Le programme serveur est spécifié au moyen d'un identificateur de programme ou *ProgID*. Le serveur utilise ce *ProgID* ainsi que le Registre du serveur pour localiser les informations relatives au programme à exécuter.

En interne, RDS fait une distinction selon que le programme serveur est installé sur un serveur distant sur Internet ou un intranet, sur un serveur sur un réseau local ou qu’il n’est pas installé sur un serveur mais sur une bibliothèque de liens dynamiques (DLL). En faisant cette distinction, RDS détermine la façon dont les informations sont échangées entre le client et le serveur et retourne des références différentes à votre application. Cependant, en ce qui vous concerne, cette distinction est transparente et sans importance puisque vous recevez de toute façon une référence de programme exploitable.

## <a name="rdsserverdatafactory"></a>RDSServer.DataFactory

RDS fournit un programme serveur par défaut capable d’exécuter des requêtes SQL sur la source de données et de retourner un objet [Recordset](recordset-object-ado.md) ou de prendre un objet **Recordset** et de mettre à jour la source de données.

Le modèle objet RDS fournit cette fonctionnalité grâce à l'objet [RDSServer.DataFactory](datafactory-object-rdsserver.md).

En outre, cet objet dispose d’une méthode pour créer un objet **Recordset** vide que vous pouvez remplir par programme ([CreateRecordset](createrecordset-method-rds.md)), et d’une autre méthode pour convertir un objet **Recordset** en chaîne de texte pour créer une page web ([ConvertToString](converttostring-method-rds.md)).

ADO vous permet de remplacer une partie du comportement de commande et de connexion standard de **RDSServer.DataFactory** grâce à un gestionnaire **DataFactory** et à un fichier de personnalisation qui contient les paramètres de connexion, de commande et de sécurité.

Le programme serveur est parfois désigné par le terme *objet métier*. Vous pouvez écrire un objet métier pour effectuer des opérations plus complexes d'accès aux données, des contrôles de validité, etc. Même si vous écrivez votre propre objet métier, vous pouvez créer une instance d'un objet **RDSServer.DataFactory** et utiliser certaines de ses méthodes pour réaliser vos propres tâches.

## <a name="rdsdatacontrol"></a>RDS. DataControl

RDS offre la possibilité de combiner les fonctionnalités de **RDS.DataSpace** et de **RDSServer.DataFactory** et permet aux contrôles visuels d'utiliser facilement l'objet **Recordset** retourné par une requête exécutée sur une source de données. Dans la plupart des cas, RDS tente d'accéder automatiquement aux informations sur le serveur et de les afficher dans un contrôle visuel.

Le modèle objet RDS fournit ces fonctionnalités grâce à l'objet [RDS.DataControl](datacontrol-object-rds.md).

L'objet **RDS.DataControl** présente deux aspects. Le premier porte sur la source de données. Si vous définissez les informations de connexion et de commande à l'aide des propriétés **Connect** et **SQL** de l'objet **RDS.DataControl**, la source de données utilise automatiquement l'objet **RDS.DataSpace** pour créer une référence à l'objet **RDSServer.DataFactory** par défaut. Puis, l'objet **RDSServer.DataFactory** utilise la valeur de la propriété **Connect** pour établir la connexion à la source de données et la valeur de la propriété **SQL** pour obtenir un objet **Recordset** à partir de la source de données et retourne l'objet **Recordset** à l'objet **RDS.DataControl**.

Le second aspect porte sur l'affichage des informations de l'objet **Recordset** retournées dans un contrôle visuel. Vous pouvez associer un contrôle visuel au **rdS. DataControl** (dans un processus appelé liaison) et accéder aux informations dans l’objet **Recordset** associé, affichant les résultats de la requête sur une page web dans Microsoft Internet Explorer. Chaque objet **RDS.DataControl** lie un objet **Recordset**, représentant les résultats d'une seule requête, à un ou plusieurs contrôles visuels (par exemple, une zone de texte, une zone de liste déroulante, un contrôle Grid, etc.). Une page peut comporter plusieurs objets **RDS.DataControl**. Chaque objet **RDS.DataControl** peut être connecté à une source de données différente et contenir les résultats d'une requête distincte.

L'objet **RDS.DataControl** comporte ses propres méthodes de navigation, de tri et de filtrage des lignes de l'objet **Recordset** associé. Ces méthodes, bien que similaires à celles de l'objet **Recordset** ADO, présentent quelques différences.

## <a name="events"></a>Événements

RDS prend en charge deux événements qui lui sont propres et indépendants du modèle d'événement ADO. [L’événement onReadyStateChange](onreadystatechange-event-rds.md) est appelé chaque fois que **rdS. Modification de** [la propriété DataControl ReadyState,](readystate-property-rds.md) vous notifiant ainsi lorsqu’une opération asynchrone s’est correctement terminée, terminée ou a connu une erreur. L'événement [onError](onerror-event-rds.md) est appelé chaque fois qu'une erreur se produit, même si l'erreur se produit au cours d'une opération asynchrone.

> [!NOTE]
> [!REMARQUE] Microsoft Internet Explorer fournit à RDS deux événements supplémentaires : **onDataSetChanged** (l'objet **Recordset** est fonctionnel mais n'a pas terminé de récupérer des lignes) et **onDataSetComplete** (l'objet **Recordset** a fini de récupérer des lignes).


