---
title: Open, méthode (enregistrement ADO)
TOCTitle: Open method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 87fe3e50c6abc0d78f1bf506c02bc63829fec882
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602114"
---
# <a name="open-method-ado-record"></a>Open, méthode (enregistrement ADO)

**S’applique à** : Access 2013, Office 2013

Ouvre un objet [Record](record-object-ado.md) existant ou crée un nouvel élément représenté par l’objet **Record** (tel qu’un fichier ou un répertoire).

## <a name="syntax"></a>Syntaxe

Open *Source*, *ActiveConnection*, *Mode*, *CreateOptions*, *Options*, *UserName*, *Password*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Source* |Facultatif. Valeur de type **Variant** qui peut représenter l'URL de l'entité à représenter par cet objet **Record**, un objet **Command**, un objet [Recordset](recordset-object-ado.md) ouvert ou un autre objet **Record**, une chaîne contenant une instruction SELECT SQL ou un nom de table.|
|*ActiveConnection* | Facultatif. Valeur de type **Variant** qui représente la chaîne de connexion ou l'objet [Connection](connection-object-ado.md) ouvert.|
|*Mode* |Facultatif. Valeur [ConnectModeEnum](connectmodeenum.md) dont la valeur par défaut est **adModeUnknown**, qui spécifie le mode d'accès à l'objet **Record** résultant.|
|*CreateOptions* |Facultatif. Valeur [RecordCreateOptionsEnum](recordcreateoptionsenum.md) dont la valeur par défaut est **adFailIfNotExists**, qui spécifie si un fichier ou un répertoire existant doit être ouvert ou s’il faut créer un nouveau fichier ou répertoire. Si la valeur par défaut est définie, le mode d’accès est obtenu de la propriété [Mode](mode-property-ado.md). Ce paramètre n’est pas pris en compte lorsque le paramètre *Source* ne contient pas d’URL.|
|*Options* |Facultatif. Valeur [RecordOpenOptionsEnum](recordopenoptionsenum.md) dont la valeur par défaut est **adOpenRecordUnspecified**, qui spécifie des options pour ouvrir l'objet **Record**. Il est possible de combiner ces valeurs.|
|*UserName* |Facultatif. Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Source*.|
|*Password* |Facultatif. Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.|

## <a name="remarks"></a>Remarques

*Source* peut représenter les éléments suivants :

- URL. Si le protocole de l'URL est http, le fournisseur Internet est appelé par défaut. Si l'URL pointe vers un nœud qui contient un script exécutable (tel qu'une page .ASP), un objet **Record** contenant la source au lieu du contenu exécuté est ouvert par défaut. Utilisez l'argument *Options* pour modifier ce comportement.

- Objet **Record**. Un objet **Record** ouvert à partir d'un autre objet **Record** clone l'objet **Record** d'origine.

- Objet **Command**. L'objet **Record** ouvert représente la seule ligne retournée par l'exécution de **Command**. Si les résultats contiennent plusieurs lignes, le contenu de la première est placé dans l'enregistrement et une erreur peut être ajoutée à la collection **Errors**.

- Instruction SELECT SQL. L'objet **Record** ouvert représente la seule ligne retournée par l'exécution du contenu de la chaîne. Si les résultats contiennent plusieurs lignes, le contenu de la première est placé dans l'enregistrement et une erreur peut être ajoutée à la collection **Errors**.

- Nom de table

Si l'objet **Record** représente une entité à laquelle il n'est pas possible d'accéder avec une URL (par exemple une ligne d'un objet **Recordset** dérivé d'une base de données), les valeurs de la propriété [ParentURL](parenturl-property-ado.md) et du champ accédé avec la constante **adRecordURL** sont NULL.

> [!NOTE]
> [!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, voir [URL absolues et relatives.](absolute-and-relative-urls.md)


