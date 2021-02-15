---
title: Objet DataControl (RDS)
TOCTitle: DataControl object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ffe674f3aa02e5cc8b1f89375ca66b4efa623f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294518"
---
# <a name="datacontrol-object-rds"></a>Objet DataControl (RDS)

**S’applique à** : Access 2013, Office 2013

Lie un jeu [](recordset-object-ado.md) d’enregistrements de requête de données à un ou plusieurs contrôles (par  exemple, une zone de texte, un contrôle grille ou une zone de liste déroulante) pour afficher les données du jeu d’enregistrements sur une page web.

## <a name="syntax"></a>Syntaxe

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a>Remarques

L'identificateur de classe (Class ID) de l'objet **RDS.DataControl** est BD96C556-65A3-11D0-983A-00C04FC29E33.

> [!NOTE]
> [!REMARQUE] Si vous recevez un message d'erreur indiquant qu'un objet [RDS.DataSpace](dataspace-object-rds.md) ou **RDS.DataControl** ne se charge pas, vérifiez que vous utilisez le bon identificateur de classe. Les identificateurs de ces objets ont changé entre la version 1.0 et la version 1.1.

Dans un scénario de base, il vous suffit de définir les propriétés **SQL**, **Connect** et **Server** de l'objet **RDS.DataControl**, ce qui provoquera automatiquement un appel de l'objet métier par défaut, [RDSServer.DataFactory](datafactory-object-rdsserver.md).

Toutes les propriétés de l'objet **RDS.DataControl** sont facultatives car des objets métier personnalisés peuvent remplacer leurs fonctionnalités.

> [!NOTE]
> [!REMARQUE] Si votre requête porte sur des résultats multiples, seul le premier [Recordset](recordset-object-ado.md) (jeu d'enregistrements) est renvoyé. Si des jeux multiples de résultats sont nécessaires, affectez chacun d'entre eux à un **DataControl** individuel. 
> 
> Voici un exemple de requête pour plusieurs résultats `"Select * from Authors, Select * from Topics"` :

En ajoutant « DFMode=20; » à la chaîne de connexion lorsque vous utilisez l'objet **RDS.DataControl**, vous améliorerez les performances du serveur lors de la mise à jour des données. Avec ce paramètre, l'objet **RDSServer.DataFactory** utilise moins de ressources au niveau du serveur. Toutefois, les fonctions suivantes ne sont pas disponibles dans cette configuration :

  - utilisation de requêtes paramétrées ;

  - obtention d'informations de paramètres et de colonnes avant l'appel de la méthode **Execute**;

  - affectation de la valeur **True** à **Transact Updates**;

  - obtention de l'état des lignes ;

  - appel de la méthode [Resync](resync-method-ado.md) ;

  - actualisation (explicite ou automatique) via la propriété [Update Resync](update-resync-property-dynamic-ado.md) ;

  - définition des propriétés **Command** ou [Recordset](recordset-sourcerecordset-properties-rds.md) ;

  - utilisation d' **adCmdTableDirect**.

L'objet **RDS.DataControl** s'exécute en mode asynchrone par défaut. Si l'exécution synchrone est requise pour votre application, affectez au paramètre [ExecuteOptions](executeoptions-property-rds.md) la valeur **adcExecSync** et au paramètre [FetchOptions](fetchoptions-property-rds.md) la valeur **adcFetchUpFront**, comme indiqué dans l'exemple suivant.

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
        ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
       <PARAM NAME="ExecuteOptions" VALUE="1">
       <PARAM NAME="FetchOptions" VALUE="1">
    </OBJECT>
```

Utilisez un objet **RDS.DataControl** pour lier les résultats d'une seule requête à un ou plusieurs contrôles visuels. Par exemple, supposons que vous écriviez une requête visant à obtenir des données client comme le nom, l'adresse, le lieu de naissance, l'âge et le statut prioritaire du client. Vous pouvez utiliser un seul objet **RDS.DataControl** pour afficher le nom, l'âge et la région dans trois zones de texte distinctes, le statut prioritaire sous la forme d'une case à cocher et toutes les données dans un contrôle de grille.

Utilisez des objets **RDS.DataControl** différents pour lier les résultats de requêtes multiples à des contrôles visuels distincts. Supposons par exemple que vous utilisiez une requête pour obtenir des informations sur un client et une deuxième requête pour obtenir des informations sur les articles achetés par ce client. Vous voulez afficher les résultats de la première requête dans trois zones de texte et à l'aide d'une case à cocher, et ceux de la deuxième requête dans un contrôle de grille. Si vous utilisez l'objet métier par défaut (**RDSServer.DataFactory**), vous devez procéder comme suit :

  - Ajoutez **deux rds. Objets DataControl** sur votre page web.

  - Rédiger deux requêtes, une pour chaque propriété **SQL** des deux objets **RDS.DataControl**. Un objet **RDS.DataControl** contiendra une requête SQL demandant des informations client ; le deuxième objet contiendra une requête demandant la liste des articles achetés par le client.

  - Dans chaque balise OBJECT des contrôles liés, indiquez la valeur DATAFLD pour définir les valeurs des données à afficher dans chaque contrôle visuel.

Il n’existe aucune restriction de nombre sur le nombre **de RDS. Objets DataControl** que vous pouvez incorporer via des balises OBJECT sur une seule page web.

Lorsque vous définissez **le rds. Objet DataControl** sur une page web,  utilisez des valeurs de hauteur et de largeur autres que 1 (pour éviter l’inclusion d’espace supplémentaire). 

Les composants clients Remote Data Service sont déjà inclus dans Internet Explorer 4.0 ; vous n'avez donc pas besoin d'inclure un paramètre CODEBASE dans votre balise d'objet **RDS.DataControl**.

Avec Internet Explorer 4.0 ou une ultérieure, vous pouvez lier des données à l’aide de contrôles HTML et de contrôles ActiveX uniquement s’ils sont marqués comme des contrôles de modèle d’appart.

**Utilisateurs Visual Basic Microsoft** The **RDS. DataControl est** utilisé uniquement dans les applications web. Les applications clientes Visual Basic n'en ont pas besoin.

