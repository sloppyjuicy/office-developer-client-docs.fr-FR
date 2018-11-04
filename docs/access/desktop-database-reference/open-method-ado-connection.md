---
title: Open, méthode (connexion ADO)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66a62128a8ad8828c501cdaf899448edd9f1d37f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949872"
---
# <a name="open-method-ado-connection"></a>Open, méthode (connexion ADO)

**S’applique à**: Access 2013, Office 2013
 
Ouvre une connexion à une source de données.

## <a name="syntax"></a>Syntaxe

*connexion*. Ouvrez*ConnectionString*, *UserID*, *le mot de passe*, *Options*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*ConnectionString* |Facultatif. Valeur de type **String** contenant des informations de connexion. Consultez la propriété [ConnectionString](connectionstring-property-ado.md) pour en savoir plus sur les paramètres valides.|
|*Nom d’utilisateur* |Facultatif. Valeur de type **String** contenant le nom d'utilisateur à employer lors de l'établissement de la connexion.|
|*Password* |Facultatif. Valeur de type **String** contenant le mot de passe à employer lors de l'établissement de la connexion.|
|*Options* |Facultatif. Valeur [ConnectOptionEnum](connectoptionenum.md) qui détermine si cette méthode doit être exécutée après l'établissement de la connexion (de façon synchrone) ou avant (de façon asynchrone).|

## <a name="remarks"></a>Notes

L'utilisation de la méthode **Open** sur un objet [Connection](connection-object-ado.md) établit la connexion physique à une source de données. Une fois l'exécution de la méthode terminée, la connexion est active et vous pouvez exécuter des commandes sur cette connexion et traiter les résultats.

Utilisez l’argument facultatif *ConnectionString* pour spécifier une chaîne de connexion contenant une série d’instructions *argument* *= valeur* séparées par des points-virgules, ou un fichier ou une ressource de répertoire identifiée par une URL. La propriété **ConnectionString** hérite automatiquement de la valeur utilisée pour l’argument *ConnectionString* . Par conséquent, vous pouvez définir la propriété **ConnectionString** de l’objet **Connection** avant de l’ouvrir, ou utilisez l’argument *ConnectionString* pour définir ou substituer les paramètres de connexion en cours pendant l’appel de méthode **Open** .

Si vous passez des données de mot de passe et d'utilisateur dans l'argument *ConnectionString* et dans les arguments facultatifs *UserID* et *Password*, les arguments *UserID* et *Password* se substituent aux valeurs spécifiées dans l'argument *ConnectionString*.

Une fois vos opérations sur l’objet **Connection** ouvert terminées, utilisez la méthode [Close](close-method-ado.md) pour libérer les ressources système associées. La fermeture d’un objet ne le supprime pas de la mémoire  ; vous pouvez modifier ses paramètres de propriétés et utiliser la méthode **Open** pour le rouvrir ultérieurement. Pour éliminer complètement un objet de la mémoire, vous devez définir la variable objet à *Nothing*.

**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet de **connexion** côté client, la méthode **Open** n’établit pas effective une connexion au serveur jusqu'à ce qu’un [objet Recordset](recordset-object-ado.md) est ouvert sur l’objet **Connection** .

> [!NOTE]
> [!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).


