---
title: Open, méthode (Recordset ADO)
TOCTitle: Open method (ADO Recordset)
ms:assetid: 87ef19a4-28e1-dec7-ed33-4ae500b9c460
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249591(v=office.15)
ms:contentKeyID: 48546119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 02fbf58a324d6c599d5799cc42b7f049bebb1f7b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369426"
---
# <a name="open-method-ado-recordset"></a>Open, méthode (Recordset ADO)

**S’applique à** : Access 2013, Office 2013

Ouvre un curseur.

## <a name="syntax"></a>Syntaxe

*recordset*. *OpenSource*, *ActiveConnection*, *CursorType*, *LockType*, *Options*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Source* |Facultatif. Valeur de type **Variant** qui représente un objet [Command](command-object-ado.md), une instruction SQL, un nom de table, un appel de procédure stockée, une URL ou le nom d'un fichier ou objet [Stream](stream-object-ado.md) contenant un objet [Recordset](recordset-object-ado.md) stocké de façon permanente.|
|*ActiveConnection* |Facultatif. Valeur de type **Variant** qui représente un nom de variable objet [Connection](connection-object-ado.md) valide ou valeur de type **String** qui contient les paramètres de la propriété [ConnectionString](connectionstring-property-ado.md).|
|*CursorType* |Facultatif. Valeur [CursorTypeEnum](cursortypeenum.md) déterminant le type de curseur que le fournisseur doit utiliser pour ouvrir l'objet **Recordset**. La valeur par défaut est **adOpenForwardOnly**.|
|*LockType* |Facultatif. Valeur [LockTypeEnum](locktypeenum.md) déterminant le type de verrouillage (accès concurrentiel) que le fournisseur doit utiliser pour ouvrir l'objet **Recordset**. La valeur par défaut est **adLockReadOnly**.|
|*Options* |Facultatif. Valeur de type **Long** spécifiant comment le fournisseur doit retourner l’argument *Source* s’il représente autre chose qu’un objet **Command** ou indiquant que l’objet **Recordset** doit être restauré à partir d’un fichier dans lequel il a été précédemment enregistré. Il peut représenter une ou plusieurs valeurs [CommandTypeEnum](commandtypeenum.md) ou [ExecuteOptionEnum](executeoptionenum.md), lesquelles peuvent être combinées avec un opérateur de bits AND.|

> [!NOTE]
> [!REMARQUE] Si vous ouvrez un objet **Recordset** à partir d'un objet **Stream** contenant un objet **Recordset** persistant, l'utilisation d'une valeur **ExecuteOptionEnum** **adAsyncFetchNonBlocking** n'aura aucune incidence ; l'extraction sera synchrone et bloquante.

Les valeurs **adExecuteNoRecords** ou **adExecuteStream** de **ExecuteOpenEnum** ne doivent pas être utilisées avec **Open**.

## <a name="remarks"></a>Remarques

Le curseur par défaut d'un objet **Recordset** ADO est un curseur en lecture seule, avant uniquement et situé sur le serveur.

L'utilisation de la méthode **Open** sur un objet **Recordset** ouvre un curseur qui représente des enregistrements d'une table de base, les résultats d'une requête ou un objet **Recordset** précédemment enregistré.

Utilisez l'argument *Source* facultatif pour spécifier une source de données à l'aide d'un des éléments suivants : variable objet **Command**, instruction SQL, procédure stockée, nom de table, URL ou nom de chemin d'accès complet d'un fichier. Si *source* est un nom de chemin d’accès de fichier, il peut s’agit d’un chemin d’accès complet (« c:\\dirfile.rst\\ »),\\ d’un chemin d’accès relatif (« . file.rst »), ou une URL (« https://files/file.rst »).

Il est déconseillé d’utiliser l’argument *Source* de la méthode **Open** pour exécuter une requête Action qui ne retourne pas d’enregistrement car il est toujours difficile de déterminer si l’appel a réussi ou échoué. L’objet **Recordset** retourné par ce type de requête sera fermé. Appelez plutôt la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) d’un objet **Command** ou la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) d’un objet **Connection** pour exécuter une requête qui ne retourne pas d’enregistrement, comme une instruction INSERT SQL.

L’argument *ConnexionActive* correspond à la propriété [ActiveConnection](activeconnection-property-ado.md) et spécifie la connexion dans laquelle ouvrir l’objet **Recordset**. Si vous transférez une définition de connexion pour cet argument, ADO ouvre une nouvelle connexion à l'aide des paramètres spécifiés. Après avoir ouvert le **recordset** avec un curseur côté client (**CursorLocationadUseClient** = ), vous pouvez modifier la valeur de cette propriété pour envoyer des mises à jour à un autre fournisseur. Vous pouvez également attribuer la valeur **Nothing** (en Microsoft Visual Basic) ou NULL à cette propriété pour déconnecter l'objet **Recordset** de tous les fournisseurs. La modification de **ConnexionActive** pour un curseur côté serveur génère, en revanche, une erreur.

En ce qui concerne les autres arguments correspondant directement aux propriétés d'un objet **Recordset** (*Source*, *TypeCurseur* et *TypeVerrou*), la relation entre les arguments et les propriétés est la suivante :

- La propriété est en lecture/écriture avant l'ouverture de l'objet **Recordset**.
- Les paramètres de propriété sont utilisés sauf si vous passez les arguments correspondants lors de l'exécution de la méthode **Open**. Si vous passez un argument, il remplace le paramètre de propriété correspondant et le paramètre de la propriété est mis à jour avec la valeur de l'argument.
- Une fois l'objet **Recordset** ouvert, ces propriétés sont alors en lecture seule.

> [!NOTE]
> La propriété **ActiveConnection** est lue uniquement pour les objets **Recordset** dont la propriété [Source](source-property-ado-recordset.md) a pour valeur un objet **Command** valide même si l’objet **Recordset** n’est pas ouvert.

Si vous passez un objet **Command** dans l'argument *Source* et que vous passez aussi un argument *ConnexionActive*, une erreur se produit. La propriété **ActiveConnection** de l'objet **Command** doit déjà avoir pour valeur un objet **Connection** ou une chaîne de connexion valide.

Si vous passez un autre élément qu'un objet **Command** dans l'argument *Source*, vous pouvez utiliser l'argument *Options* pour optimiser l'évaluation de l'argument *Source*. Si l'argument *Options* n'est pas défini, il se peut que les performances diminuent car ADO doit passer des appels au fournisseur afin de déterminer si l'argument est une instruction SQL, une procédure stockée ou un nom de table. SI vous connaissez le type d'argument *Source* utilisé, la définition de l'argument *Options* permet à ADO d'accéder directement au code approprié. Si l'argument *Options* ne correspond pas au type de l'argument *Source*, une erreur se produit.

Si vous passez un objet **Stream** dans l'argument *Source*, ne passez pas d'informations dans les autres arguments. Si vous le faites, une erreur sera générée. Les informations du paramètre **ConnexionActive** ne sont pas conservées lorsqu'un objet **Recordset** est ouvert à partir d'un objet **Stream**.

La valeur par défaut de l'argument *Options* est **adCmdFile** si aucune connexion n'est associée à l'objet **Recordset**. C'est généralement le cas des objets **Recordset** stockés de façon permanente.

Si la source de données ne retourne aucun enregistrement, le fournisseur affecte aux propriétés [BOF](bof-eof-properties-ado.md) et [EOF](bof-eof-properties-ado.md) la valeur **True** et la position d'enregistrement actif n'est pas définie. Vous pouvez néanmoins ajouter de nouvelles données à cet objet **Recordset** vide si le type de curseur le permet.

Lorsque vous avez terminé les opérations relatives à un objet **Recordset** ouvert, utilisez la méthode [Close](close-method-ado.md) pour libérer les ressources système associées. La fermeture d’un objet ne le supprime pas de la mémoire ; vous pouvez modifier les paramètres de ses propriétés et utiliser la méthode **Open** pour le rouvrir ultérieurement. Pour éliminer définitivement un objet de la mémoire, attribuez à la variable objet la valeur *Nothing*.

Avant de **définir la propriété ActiveConnection** , appelez **Open** sans opérande pour créer une instance d’un jeu **d’enregistrements** créée en axant des champs à la collection **Recordset** [Fields](fields-collection-ado.md) .

Si vous avez attribué à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**, vous disposez de deux possibilités pour récupérer des lignes de façon asynchrone. La méthode recommandée consiste à attribuer à *Options* la valeur **adAsyncFetch**. Vous pouvez, par ailleurs, utiliser la propriété dynamique « Asynchronous Rowset Processing » dans la collection [Properties](properties-collection-ado.md) mais il se peut que vous perdiez des événements récupérés si vous n'attribuez pas au paramètre **Options** la valeur **adAsyncFetch**.

> [!NOTE]
> L'extraction en arrière-plan dans le fournisseur distant Microsoft est pris en charge uniquement par le paramètre *Options* de la méthode **Open**.

> [!NOTE]
> Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, voir [URL absolues et relatives](absolute-and-relative-urls.md).
