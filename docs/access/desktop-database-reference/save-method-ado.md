---
title: Save, méthode - ActiveX Data Objects (ADO)
TOCTitle: Save method (ADO)
ms:assetid: 02dab13b-f947-b96d-46ea-0def3ed8f28f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248793(v=office.15)
ms:contentKeyID: 48542968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 86d164a133538379a15c80f7fb5f2f4ba71267bf
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950208"
---
# <a name="save-method-ado"></a>Save, méthode (ADO)

**S’applique à**: Access 2013, Office 2013

Enregistre l'objet [Recordset](recordset-object-ado.md) dans un fichier ou un objet [Stream](stream-object-ado.md).

## <a name="syntax"></a>Syntaxe

*jeu d’enregistrements*. Enregistrer la*Destination*, *PersistFormat*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Destination* |Facultatif. Valeur de type **Variant** qui représente le nom de chemin d'accès complet du fichier dans lequel l'objet **Recordset** doit être enregistré ou une référence à l'objet **Stream**.|
|*PersistFormat* |Facultatif. Valeur [PersistFormatEnum](persistformatenum.md) qui spécifie le format d'enregistrement de l'objet **Recordset** (XML ou ADTG). La valeur par défaut est **adPersistADTG**.|

## <a name="remarks"></a>Notes

La méthode **Save** peut uniquement être appelée sur un objet **Recordset** ouvert. Utilisez la méthode [Open](open-method-ado-recordset.md) pour restaurer ultérieurement l’objet **Recordset** à partir de *Destination*.

Si la propriété [Filter](filter-property-ado.md) est appliquée pour l'objet **Recordset**, seules les lignes accessibles sous le filtre sont enregistrées. Si l'objet **Recordset** est hiérarchique, l'objet **Recordset** enfant actif et ses enfants sont enregistrés, y compris l'objet **Recordset** parent. Si la méthode **Save** d'un objet **Recordset** enfant est appelée, l'enfant et tous ses enfants sont enregistrés mais pas l'objet parent.

La première fois que vous enregistrez le **jeu d’enregistrements**, il n’est pas nécessaire d’indiquer une *destination*. Si vous oubliez la *destination*, un nouveau fichier est créé et nommé selon la valeur de la propriété [Source](source-property-ado-recordset.md) du **jeu d’enregistrements**.

Omettez la *Destination* lorsque vous appelez ensuite **Enregistrer** après le premier enregistrement, ou une erreur d’exécution se produit. Si vous appelez ensuite **Enregistrer** avec une nouvelle *Destination*, l' **objet Recordset** est enregistré dans la nouvelle destination. Toutefois, la nouvelle destination et la destination d'origine seront toutes deux ouvertes.

Dans la mesure où **Save** ne ferme pas l'objet **Recordset** ni *Destination*, vous pouvez continuer à travailler avec l'objet **Recordset** et enregistrer vos modifications les plus récentes. Le paramètre *Destination* reste ouvert jusqu'à la fermeture de l'objet **Recordset**.

Pour des raisons de sécurité, la méthode **Save** autorise uniquement l'utilisation de paramètres de sécurité basse et personnalisée à partir d'un script exécuté par Microsoft Internet Explorer. Pour obtenir une explication plus détaillée des problèmes de sécurité, consultez l'article traitant des problèmes de sécurité ADO et RDS dans Microsoft Internet Explorer, figurant dans la rubrique des articles techniques sur les objets ADO (ActiveX Data Object) dans la base des articles techniques traitant de l'accès aux données.

Si une méthode **Save** est invoquée alors qu'une opération asynchrone de mise à jour, d'exécution ou d'extraction d'un **jeu d'enregistrements** est en cours, la méthode **Save** attend la fin de l'opération asynchrone.

Les enregistrements sont enregistrés en commençant par la première ligne de l'objet **Recordset**. Une fois l'exécution de la méthode **Save** terminée, la position de ligne active est déplacée à la première ligne de l'objet **Recordset**.

Pour obtenir de meilleurs résultats, affectez à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient** avec la méthode **Save**. Si votre fournisseur ne prend pas en charge toutes les fonctionnalités nécessaires à l'enregistrement des objets **Recordset**, le service de curseur les fournira.

Lorsqu'un objet **Recordset** est conservé avec la propriété **CursorLocation** affectée de la valeur **adUseServer**, les fonctionnalités de mise à jour de l'objet **Recordset** sont limitées. En général, seules les mises à jour, les insertions et les suppressions de table unique sont autorisées (selon les fonctionnalités du fournisseur). La méthode [Resync](resync-method-ado.md) n'est pas non plus disponible avec une telle configuration.

> [!NOTE]
> [!REMARQUE] L'enregistrement d'un objet **Recordset** avec des **champs** de type **adVariant**, **adIDispatch** ou **adIUnknown** n'est pas pris en charge par ADO et peut avoir des résultats imprévisibles.

Seuls les **filtres** sous la forme de chaînes de critères (P.ex \> ' 12/31/1999 ') affectent le contenu du **jeu d’enregistrements**persistant. Les filtres créés avec un tableau de **signets** ou en utilisant une valeur provenant de **FilterGroupEnum** n’affectent pas le contenu du **jeu d’enregistrements**persistant. Ces règles s'appliquent aux **jeux d'enregistrements** créés avec des curseurs côté client ou côté serveur.

Étant donné que le paramètre *Destination* accepte tout objet qui prend en charge l’interface OLE DB IStream, vous pouvez enregistrer un **objet Recordset** directement dans l’objet ASP Response. Pour plus d'informations, consultez [Scénario de persistance des objets Recordset XML](xml-recordset-persistence-scenario.md).

Vous pouvez également enregistrer un objet **Recordset** au format XML dans une instance d'un objet DOM MSXML, comme l'illustre le code Visual Basic suivant :

> [!NOTE]
> [!REMARQUE] L'enregistrement des objets **Recordset** hiérarchiques (formes de données) au format XML est assorti de deux limitations. Vous ne pouvez pas enregistrer au format XML si l'objet **Recordset** hiérarchique contient des mises à jour en attente et vous ne pouvez pas enregistrer un objet **Recordset** hiérarchique paramétré.

Un jeu d'enregistrements enregistré au format XML est enregistré à l'aide du format UTF-8. Lorsque ce type de fichier est chargé dans un flux ADO, l'objet Stream ne tente pas d'ouvrir l'objet Recordset à partir du flux sauf si la propriété Charset du flux a la valeur appropriée pour le format UTF-8.

