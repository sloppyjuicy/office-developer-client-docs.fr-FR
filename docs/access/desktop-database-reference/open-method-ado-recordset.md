---
title: Open, méthode (Recordset ADO)
TOCTitle: Open method (ADO Recordset)
ms:assetid: 87ef19a4-28e1-dec7-ed33-4ae500b9c460
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249591(v=office.15)
ms:contentKeyID: 48546119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e0d5302291f1514fd11bca8fe7094af4525c900
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026476"
---
# <a name="open-method-ado-recordset"></a>Open, méthode (Recordset ADO)

**S’applique à**: Access 2013, Office 2013

Ouvre un curseur.

## <a name="syntax"></a>Syntaxe

*jeu d’enregistrements*. Ouvrir la*Source*, *ActiveConnection*, *CursorType*, *LockType*, *Options*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Source* |Facultatif. Valeur de type **Variant** qui représente un objet [Command](command-object-ado.md), une instruction SQL, un nom de table, un appel de procédure stockée, une URL ou le nom d'un fichier ou objet [Stream](stream-object-ado.md) contenant un objet [Recordset](recordset-object-ado.md) stocké de façon permanente.|
|*ActiveConnection* |Facultatif. Valeur de type **Variant** qui représente un nom de variable objet [Connection](connection-object-ado.md) valide ou valeur de type **String** qui contient les paramètres de la propriété [ConnectionString](connectionstring-property-ado.md).|
|*CursorType* |Facultatif. Valeur [CursorTypeEnum](cursortypeenum.md) déterminant le type de curseur que le fournisseur doit utiliser pour ouvrir l'objet **Recordset**. La valeur par défaut est **adOpenForwardOnly**.|
|*LockType* |Facultatif. Valeur [LockTypeEnum](locktypeenum.md) déterminant le type de verrouillage (accès concurrentiel) que le fournisseur doit utiliser pour ouvrir l'objet **Recordset**. La valeur par défaut est **adLockReadOnly**.|
|*Options* |Facultatif. Une valeur de **type Long** qui indique comment le fournisseur doit évaluer l’argument *Source* si il représente autre chose qu’un objet **Command** ou **Recordset** doit être restauré à partir d’un fichier dans lequel il a été précédemment enregistré. Il peut représenter une ou plusieurs valeurs [CommandTypeEnum](commandtypeenum.md) ou [ExecuteOptionEnum](executeoptionenum.md), lesquelles peuvent être combinées avec un opérateur de bits AND.|

> [!NOTE]
> [!REMARQUE] Si vous ouvrez un objet **Recordset** à partir d'un objet **Stream** contenant un objet **Recordset** persistant, l'utilisation d'une valeur **ExecuteOptionEnum** **adAsyncFetchNonBlocking** n'aura aucune incidence ; l'extraction sera synchrone et bloquante.

Les valeurs **adExecuteNoRecords** ou **adExecuteStream** de **ExecuteOpenEnum** ne doivent pas être utilisées avec **Open**.

## <a name="remarks"></a>Notes

Le curseur par défaut d'un objet **Recordset** ADO est un curseur en lecture seule, avant uniquement et situé sur le serveur.

L'utilisation de la méthode **Open** sur un objet **Recordset** ouvre un curseur qui représente des enregistrements d'une table de base, les résultats d'une requête ou un objet **Recordset** précédemment enregistré.

Utilisez l’argument *Source* facultatif pour spécifier une source de données à l’aide d’une des opérations suivantes : une variable d’objet **Command** , une instruction SQL, une procédure stockée, un nom de table, une URL ou un nom de chemin d’accès complet du fichier. Si la *Source* est un nom de chemin d’accès de fichier, il peut être un chemin d’accès complet (« c :\\dir\\file.rst »), un chemin d’accès relatif («... \\file.rst »), ou une URL («https://files/file.rst»).

Il n’est pas conseillé d’utiliser l’argument *Source* de la méthode **Open** pour exécuter une requête action qui ne renvoie pas d’enregistrements, car il n’existe aucun moyen simple pour déterminer si l’appel a réussi. L'objet **Recordset** retourné par ce type de requête sera fermé. Appelez plutôt la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) d'un objet **Command** ou la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) d'un objet **Connection** pour exécuter une requête qui ne retourne pas d'enregistrement, comme une instruction INSERT SQL.

L’argument *ActiveConnection* correspond à la propriété [ActiveConnection](activeconnection-property-ado.md) et spécifie la connexion dans laquelle ouvrir le **jeu d’enregistrements** de l' objet. Si vous passez une définition de connexion pour cet argument, ADO ouvre une nouvelle connexion à l'aide des paramètres spécifiés. Après l’ouverture de l' **objet Recordset** avec un curseur côté client (**CursorLocation** = **adUseClient**), vous pouvez modifier la valeur de cette propriété pour envoyer des mises à jour à un autre fournisseur. Vous pouvez également attribuer la valeur **Nothing** (en Microsoft Visual Basic) ou NULL à cette propriété pour déconnecter l'objet **Recordset** de tous les fournisseurs. La modification de **ConnexionActive** pour un curseur côté serveur génère, en revanche, une erreur.

En ce qui concerne les autres arguments correspondant directement aux propriétés d'un objet **Recordset** (*Source*, *TypeCurseur* et *TypeVerrou*), la relation entre les arguments et les propriétés est la suivante :

- La propriété est en lecture/écriture avant l'ouverture de l'objet **Recordset**.

- Les paramètres de propriété sont utilisés sauf si vous passez les arguments correspondants lors de l'exécution de la méthode **Open**. Si vous passez un argument, il remplace le paramètre de propriété correspondant et le paramètre de la propriété est mis à jour avec la valeur de l'argument.

- Une fois l'objet **Recordset** ouvert, ces propriétés sont alors en lecture seule.

> [!NOTE]
> [!REMARQUE] La propriété **ActiveConnection** est lue uniquement pour les objets **Recordset** dont la propriété [Source](source-property-ado-recordset.md) a pour valeur un objet **Command** valide même si l'objet **Recordset** n'est pas ouvert.

Si vous passez un objet **Command** dans l’argument *Source* et également transmettez un argument *ConnexionActive* , une erreur se produit. La propriété **ActiveConnection** de l'objet **Command** doit déjà avoir pour valeur un objet **Connection** ou une chaîne de connexion valide.

Si vous passez un élément autre qu’un objet **Command** dans l’argument *Source* , vous pouvez utiliser l’argument *Options* pour optimiser l’évaluation de l’argument *Source* . Si l’argument *Options* n’est pas défini, vous pouvez rencontrer des performances car ADO doit effectuer des appels au fournisseur pour déterminer si l’argument est une instruction SQL, une procédure stockée, une URL ou un nom de table. Si vous connaissez le type de *Source* , vous utilisez, définissant l’argument *Options* indique à ADO d’accéder directement au code approprié. Si l’argument *Options* ne correspond pas du type de *Source* , une erreur se produit.

Si vous passez un objet **Stream** dans l’argument *Source* , vous ne devez pas passer d’informations dans les autres arguments. Si vous le faites, une erreur sera générée. Les informations du paramètre **ConnexionActive** ne sont pas conservées lorsqu'un objet **Recordset** est ouvert à partir d'un objet **Stream**.

La valeur par défaut pour l’argument *Options* est **adCmdFile** si aucune connexion n’est associée à l' **objet Recordset**. C'est généralement le cas des objets **Recordset** stockés de façon permanente.

Si la source de données ne retourne aucun enregistrement, le fournisseur affecte aux propriétés [BOF](bof-eof-properties-ado.md) et [EOF](bof-eof-properties-ado.md) la valeur **True** et la position d'enregistrement actif n'est pas définie. Vous pouvez néanmoins ajouter de nouvelles données à cet objet **Recordset** vide si le type de curseur le permet.

Lorsque vous avez terminé les opérations relatives à un objet **Recordset** ouvert, utilisez la méthode [Close](close-method-ado.md) pour libérer les ressources système associées. La fermeture d’un objet ne le supprime pas de la mémoire ; vous pouvez modifier les paramètres de ses propriétés et utiliser la méthode **Open** pour le rouvrir ultérieurement. Pour éliminer définitivement un objet de la mémoire, attribuez à la variable objet la valeur *Nothing*.

Avant de définie la propriété **ActiveConnection** , appelez la fonction **Open** sans opérande pour créer une instance d’un **objet Recordset** créée par l’ajout de champs à la collection de [champs](fields-collection-ado.md) du **jeu d’enregistrements** .

Si vous avez attribué à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**, vous disposez de deux possibilités pour récupérer des lignes de façon asynchrone. La méthode recommandée consiste à définir les *Options* **valeur adAsyncFetch**. Vous pouvez, par ailleurs, utiliser la propriété dynamique « Asynchronous Rowset Processing » dans la collection [Properties](properties-collection-ado.md) mais il se peut que vous perdiez des événements récupérés si vous n'attribuez pas au paramètre **Options** la valeur **adAsyncFetch**.

> [!NOTE]
> Extraction en arrière-plan dans le fournisseur MS Remote est pris en charge uniquement par le paramètre *Options* de la méthode **Open** .

> [!NOTE]
> [!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).


