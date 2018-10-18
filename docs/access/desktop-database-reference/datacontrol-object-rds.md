---
title: DataControl, objet (RDS)
TOCTitle: DataControl Object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3382b86ad14b484cb0fb9a8f6ecbd95018c25835
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607010"
---
# <a name="datacontrol-object-rds"></a>DataControl, objet (RDS)

**S’applique à**: Access 2013 | Office 2013

<<<<<<< Tête lie un données requête [jeu d’enregistrements](recordset-object-ado.md) à un ou plusieurs contrôles (par exemple, une zone de texte, contrôle de grille ou zone de liste déroulante) pour afficher les données du **jeu d’enregistrements** dans une page Web.
=== Lie un [objet Recordset](recordset-object-ado.md) de requête de données à un ou plusieurs contrôles (par exemple, une zone de texte, contrôle de grille ou zone de liste déroulante) pour afficher les données du **jeu d’enregistrements** sur une page Web.
>>>>>>> master

## <a name="syntax"></a>Syntaxe

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a>Notes

L'identificateur de classe (Class ID) de l'objet **RDS.DataControl** est BD96C556-65A3-11D0-983A-00C04FC29E33.

> [!NOTE]
> [!REMARQUE] Si vous recevez un message d'erreur indiquant qu'un objet [RDS.DataSpace](dataspace-object-rds.md) ou **RDS.DataControl** ne se charge pas, vérifiez que vous utilisez le bon identificateur de classe. Les identificateurs de ces objets ont changé entre la version 1.0 et la version 1.1.

Dans un scénario de base, il vous suffit de définir les propriétés **SQL**, **Connect** et **Server** de l'objet **RDS.DataControl**, ce qui provoquera automatiquement un appel de l'objet métier par défaut, [RDSServer.DataFactory](datafactory-object-rdsserver.md).

Toutes les propriétés de l'objet **RDS.DataControl** sont facultatives car des objets métier personnalisés peuvent remplacer leurs fonctionnalités.

> [!NOTE]
> [!REMARQUE] Si votre requête porte sur des résultats multiples, seul le premier [Recordset](recordset-object-ado.md) (jeu d'enregistrements) est renvoyé. Si des jeux multiples de résultats sont nécessaires, affectez chacun d'entre eux à un **DataControl** individuel. 
> 
> Un exemple d’une requête de résultats multiples peut être la suivante : `"Select * from Authors, Select * from Topics"`.

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

<<<<<<< Tête
  - Ajouter deux objets **RDS.DataControl** à votre page Web.
=======
  - Ajoutez deux **RDS. DataControl** objets à votre page Web.
>>>>>>> master

  - Rédiger deux requêtes, une pour chaque propriété **SQL** des deux objets **RDS.DataControl**. Un objet **RDS.DataControl** contiendra une requête SQL demandant des informations client ; le deuxième objet contiendra une requête demandant la liste des articles achetés par le client.

  - Dans chaque balise OBJECT des contrôles liés, indiquez la valeur DATAFLD pour définir les valeurs des données à afficher dans chaque contrôle visuel.

<<<<<<< Tête il n’existe aucune restriction de comptage du nombre de **RDS. DataControl** objets que vous pouvez imbriquer via des balises OBJECT dans une page Web unique.

<a name="when-you-define-the-rdsdatacontrol-object-on-a-web-page-use-nonzero-height-and-width-values-such-as-1-to-avoid-the-inclusion-of-extra-space"></a>Lorsque vous définissez l'objet **RDS.DataControl** dans une page Web, utilisez des valeurs différentes de zéro pour **Height** et **Width**, telles que 1 (pour éviter d'inclure des espaces inutiles).
=======
Il n’existe aucune restriction de comptage du nombre de **RDS. DataControl** objets que vous pouvez imbriquer via des balises OBJECT dans une seule page Web.

Lorsque vous définissez la **RDS. DataControl** d’objets sur une page Web, utilisez des valeurs différentes de zéro de **hauteur** et la **largeur** tel que 1 (pour éviter d’inclure des espaces inutiles).
>>>>>>> master

Les composants clients Remote Data Service sont déjà inclus dans Internet Explorer 4.0 ; vous n'avez donc pas besoin d'inclure un paramètre CODEBASE dans votre balise d'objet **RDS.DataControl**.

Avec Internet Explorer 4.0 ou version ultérieure, vous pouvez effectuer une liaison à des données à l'aide de contrôles HTML et ActiveX® uniquement s'ils sont identifiés comme des contrôles de modèle cloisonné.

**Utilisateurs de Microsoft Visual Basic** **RDS. DataControl** est utilisé uniquement dans les applications Web. Les applications clientes Visual Basic n'en ont pas besoin.

