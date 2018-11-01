---
title: Connection, objet (ADO)
TOCTitle: Connection Object (ADO)
ms:assetid: c16023aa-0321-2513-ee71-255d6ffba03d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249940(v=office.15)
ms:contentKeyID: 48547528
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231105
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0f2c629a24bf6327be8a9848e719b40bfa88ea17
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873319"
---
# <a name="connection-object-ado"></a>Connection, objet (ADO)

**S’applique à**: Access 2013, Office 2013

Représente une connexion ouverte à une source de données.

## <a name="remarks"></a>Notes

Un objet **Connection** représente une session unique avec une source de données. Dans le cas d'un système de base de données client/serveur, il peut être équivalent à une connexion réseau réelle au serveur. Selon les fonctionnalités prises en charge par le fournisseur, certaines collections, méthodes ou propriétés d'un objet **Connection** risquent de ne pas être disponibles.

Les collections, les méthodes et les propriétés d'un objet **Connection** vous permettent d'effectuer diverses tâches :

  - configurer la connexion avant de l'ouvrir avec les propriétés [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md) et [Mode](mode-property-ado.md) ( **ConnectionString** étant la propriété par défaut de l'objet **Connection** ) ;

  - définir le client comme valeur de la propriété [CursorLocation](cursorlocation-property-ado.md) pour appeler [Service de curseur Microsoft pour OLE DB (composant du service ADO)](microsoft-cursor-service-for-ole-db-ado-service-component.md), qui prend en charge les mises à jour par lot ;

  - définir la base de données par défaut de la connexion avec la propriété [DefaultDatabase](defaultdatabase-property-ado.md) ;

  - définir le niveau d'isolation des transactions ouvertes sur la connexion avec la propriété [IsolationLevel](isolationlevel-property-ado.md) ;

  - spécifier un fournisseur OLE DB avec la propriété [Provider](provider-property-ado.md) ;

  - établir (et ultérieurement rompre) la connexion physique à la source de données avec les méthodes [Open](open-method-ado-connection.md) et [Close](close-method-ado.md) ;

  - exécuter une commande sur la connexion avec la méthode [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) et configurer l'exécution avec la propriété [CommandTimeout](commandtimeout-property-ado.md) ;
    

    > [!NOTE]
    > [!REMARQUE] Pour exécuter une requête sans utiliser d'objet Command, passez une chaîne de requête à la méthode **Execute** d'un objet **Connection**. Toutefois, un objet [Command](command-object-ado.md) est nécessaire si vous voulez rendre persistant le texte de commande et l'exécuter de nouveau, ou utiliser des paramètres de requête.

  - gérer des transactions sur une connexion ouverte, notamment des transactions imbriquées si le fournisseur les prend en charge, avec les méthodes [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) et [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), ainsi qu'avec la propriété [Attributes](attributes-property-ado.md) ;

  - examiner les erreurs renvoyées par la source de données à l'aide de la collection [Errors](errors-collection-ado.md) ;

  - lire la version de l'implémentation ADO utilisée avec la propriété [Version](version-property-ado.md) ;

  - obtenir des informations de schéma sur votre base de données au moyen de la méthode [OpenSchema](openschema-method-ado.md).

Vous pouvez créer des objets **Connection** indépendamment de tout autre objet défini précédemment.

Vous pouvez exécuter des commandes ou des procédures stockées comme si celles-ci étaient des méthodes natives de l'objet **Connection** (voir exemples ci-dessous).

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a>Exécuter une commande comme une méthode native d'un objet Connection

Pour exécuter une commande, donnez-lui un nom à l'aide de la propriété **Name** de l'objet [Command](name-property-ado.md). Attribuez à la propriété **ActiveConnection** de l'objet **Command** le nom de la connexion. Émettez ensuite une instruction dans laquelle le nom de la commande est utilisé comme s'il s'agissait d'une méthode de l'objet **Connection**, suivie d'éventuels paramètres et ensuite d'un objet **Recordset** si des lignes sont renvoyées. Définissez les propriétés de **Recordset** de façon à personnaliser l'objet **Recordset** obtenu. Par exemple :

```vb
    Dim cnn As New ADODB.Connection
    Dim cmd As New ADODB.Command
    Dim rst As New ADODB.Recordset
    ...
    cnn.Open "..."
    cmd.Name = "yourCommandName"
    cmd.ActiveConnection = cnn
    ...
    'Your command name, any parameters, and an optional Recordset.
    cnn.yourCommandName "parameter", rst
```

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a>Exécuter une procédure stockée comme une méthode native d'un objet Connection

Pour exécuter une procédure stockée, émettez une instruction dans laquelle le nom de la procédure stockée est utilisé comme s'il s'agissait d'une méthode de l'objet **Connection**, suivie d'éventuels paramètres. ADO détermine du mieux qu'il peut les types des paramètres. Par exemple :

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
