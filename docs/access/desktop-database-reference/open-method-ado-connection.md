---
title: Open, méthode (connexion ADO)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b83eb87b181320c86e1aea91ede70cd173a5ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288426"
---
# <a name="open-method-ado-connection"></a>Open, méthode (connexion ADO)

**S’applique à** : Access 2013, Office 2013
 
Ouvre une connexion à une source de données.

## <a name="syntax"></a>Syntaxe

*.* Open *ConnectionString*, *UserID*, *Password*, *Options*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*ConnectionString* |Facultatif. Valeur de type **String** contenant des informations de connexion. Consultez la propriété [ConnectionString](connectionstring-property-ado.md) pour en savoir plus sur les paramètres valides.|
|*UserID* |Facultatif. Valeur de type **String** contenant le nom d'utilisateur à employer lors de l'établissement de la connexion.|
|*Password* |Facultatif. Valeur de type **String** contenant le mot de passe à employer lors de l'établissement de la connexion.|
|*Options* |Facultatif. Valeur [ConnectOptionEnum](connectoptionenum.md) qui détermine si cette méthode doit être exécutée après l'établissement de la connexion (de façon synchrone) ou avant (de façon asynchrone).|

## <a name="remarks"></a>Remarques

L’utilisation de la méthode **Open** sur un objet [Connection](connection-object-ado.md) établit la connexion physique à une source de données. Une fois l’exécution de la méthode terminée, la connexion est active et vous pouvez exécuter des commandes sur cette connexion et traiter les résultats.

Utilisez l’argument *ConnectionString* facultatif pour spécifier soit une chaîne de connexion contenant une série *d’arguments* *=* instructions de valeur séparées par des points-virgules, soit un fichier ou une ressource d’annuaire identifié avec une URL. La propriété **ConnectionString** hérite automatiquement de la valeur utilisée pour l'argument *ConnectionString*. Par conséquent, vous pouvez soit définir la propriété **ConnectionString** de l'objet **Connection** avant d'ouvrir celui-ci, soit utiliser l'argument *ConnectionString* pour définir ou substituer les paramètres de connexion actifs lors de l'appel de la méthode **Open**.

Si vous passez des données de mot de passe et d'utilisateur dans l'argument *ConnectionString* et dans les arguments facultatifs *UserID* et *Password*, les arguments *UserID* et *Password* se substituent aux valeurs spécifiées dans l'argument *ConnectionString*.

Une fois vos opérations sur l’objet **Connection** ouvert terminées, utilisez la méthode [Close](close-method-ado.md) pour libérer les ressources système associées. La fermeture d’un objet ne le supprime pas de la mémoire  ; vous pouvez modifier ses paramètres de propriétés et utiliser la méthode **Open** pour le rouvrir ultérieurement. Pour éliminer complètement un objet de la mémoire, vous devez définir la variable objet à *Nothing*.

**Utilisation du service de données à distance** Lorsqu’elle est utilisée sur un objet **Connection** côté client, la méthode [](recordset-object-ado.md) **Open** n’établit pas réellement de connexion au serveur tant qu’un jeu d’enregistrements n’est pas ouvert sur l’objet **Connection.**

> [!NOTE]
> Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, voir [URL absolues et relatives.](absolute-and-relative-urls.md)


