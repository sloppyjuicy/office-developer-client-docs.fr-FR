---
title: Append, méthode (ADO)
TOCTitle: Append method (ADO)
ms:assetid: cca133af-2b95-877d-0488-0d99631623f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250014(v=office.15)
ms:contentKeyID: 48547742
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a85faf900860dabb809a10a92985559b7a7cf2ef
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706078"
---
# <a name="append-method-ado"></a>Append, méthode (ADO)

**S’applique à**: Access 2013, Office 2013

Ajoute un objet à une collection. S'il s'agit de la collection [Fields](fields-collection-ado.md), un nouvel objet [Field](field-object-ado.md) peut être créé avant d'être ajouté à la collection.

## <a name="syntax"></a>Syntaxe

la *collection*. Ajouter *l’objet*

*champs*. Ajouter le *nom*, *Type*, *DefinedSize*, *attributs*, *FieldValue*

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*collection* |Objet Collection.|
|*fields* |Collection **Fields**.|
|*object* |Variable objet représentant l'objet à ajouter.|
|*Name* |Valeur **String** contenant le nom du nouvel objet **Field**. Ce nom doit être différent de ceux des autres objets de la collection *Fields*.|
|*Type* |Valeur [DataTypeEnum](datatypeenum.md) qui, par défaut, est définie à **adEmpty** et qui spécifie le type de données du nouveau champ. Les types de données suivants ne sont pas pris en charge par ADO et ne doivent pas être utilisés lors de l'ajout de nouveaux champs à un objet **Recordset**: **adIDispatch**, **adIUnknown**, **adVariant**.|
|*DefinedSize* |Facultatif. Valeur de type **Long** représentant la taille définie, en caractères ou en octets, du nouveau champ. La valeur par défaut de ce paramètre est dérivée de *Type*. Les champs dont la valeur DefinedSize est supérieure à 255 octets sont traités comme des colonnes de longueur variable. (La valeur *DefinedSize* par défaut n'est pas spécifiée.)|
|*Attrib* |Facultatif. Valeur [FieldAttributeEnum](fieldattributeenum.md), définie par défaut à **adFldDefault**, qui spécifie les attributs du nouveau champ. Si cette valeur n’est pas spécifiée, le champ contient les attributs dérivés de *Type*.|
|*FieldValue* |Facultatif. **Variant** représentant la valeur du nouveau champ. S'il n'est pas spécifié, le champ est ajouté avec la valeur Null.|

## <a name="remarks"></a>Notes

### <a name="parameters-collection"></a>Parameters, collection

Vous devez définir la propriété [Type](type-property-ado.md) d'un objet [Parameter](parameter-object-ado.md) avant de l'ajouter à la collection **Parameters**. Si vous sélectionnez un type de données de longueur variable, vous devez également attribuer une valeur supérieure à zéro à la propriété [Size](size-property-ado.md).

Lorsque vous décrivez vous-même des paramètres, vous limitez le nombre d'appels du fournisseur et vous obtenez de meilleures performances lorsque vous utilisez des procédures stockées ou des requêtes paramétrées. Toutefois, vous devez connaître les propriétés des paramètres associés à la procédure stockée ou à la requête paramétrée que vous voulez appeler.

Faites appel à la méthode [CreateParameter](createparameter-method-ado.md) pour créer des objets **Parameter** dotés des paramètres de propriété appropriés et la méthode **Append** pour les ajouter à la collection [Parameters](parameters-collection-ado.md). Vous pouvez ainsi définir et renvoyer des valeurs de paramètres sans avoir à appeler le fournisseur pour obtenir les informations appropriées. Si vous faites appel à un fournisseur qui ne fournit pas de données de paramètre, vous devez utiliser cette méthode pour remplir manuellement la collection **Parameters** sans quoi vous ne serez pas en mesure d'employer un quelconque paramètre.

### <a name="fields-collection"></a>Fields, collection

Le paramètre *FieldValue* n’est valide que lorsque vous ajoutez un objet **Field** à un objet [Record](record-object-ado.md) , pas à un objet **Recordset** . Avec un objet **Record** , vous pouvez ajouter des champs et fournir des valeurs en même temps. Avec un objet **Recordset** , vous devez créer des champs lorsque le **Recordset** est fermé, puis ouvrir le **jeu d’enregistrements** et affecter des valeurs aux champs.


> [!NOTE]
> [!REMARQUE] Pour les nouveaux objets **Field** qui ont été ajoutés à la collection **Fields** d'un objet **Record**, la propriété [Value](value-property-ado.md) doit être définie pour qu'une propriété **Field** puisse être spécifiée. Une valeur spécifique doit avoir été affectée au préalable à la propriété **Value** et la méthode [Update](update-method-ado.md) doit avoir été appelée sur la collection **Fields**. Vous pouvez alors accéder à d'autres propriétés comme [Type](type-property-ado.md) ou [Attributes](attributes-property-ado.md).


Une erreur se produit si vous tentez d'ajouter des objets **Field** ayant les types de données suivants (**DataTypeEnum**) à la collection **Fields** : **adArray**, **adChapter**, **adEmpty**, **adPropVariant** et **adUserDefined**. De même, les types de données suivants ne sont pas pris en charge par ADO : **adIDispatch**, **adIUnknown** et **adIVariant**. L'ajout de ces derniers ne génère pas d'erreur mais vous risquez d'obtenir des résultats imprévisibles et notamment des pertes de mémoire lorsque vous les utilisez.

### <a name="recordset"></a>Recordset

Si vous ne définissez pas la propriété [CursorLocation](cursorlocation-property-ado.md) avant d'appeler la méthode **Append**, **CursorLocation** prend automatiquement la valeur **adUseClient** (une valeur [CursorLocationEnum](cursorlocationenum.md)) lorsque la méthode [Open](recordset-object-ado.md) de l'objet [Recordset](open-method-ado-recordset.md) est appelée.

Vous obtenez une erreur d'exécution lorsque la méthode **Append** est appelée sur la collection **Fields** d'un objet **Recordset** ouvert ou d'un objet **Recordset** dont la propriété [ActiveConnection](activeconnection-property-ado.md) a été définie. Vous ne pouvez ajouter des champs qu'à un objet **Recordset** qui est fermé et qui n'a pas encore été connecté à une source de données. Ceci se produit, en principe, lorsqu'un objet **Recordset** est créé à l'aide d'une méthode [CreateRecordset](createrecordset-method-rds.md) ou qu'il est assigné à une variable objet.

### <a name="record"></a>Record

Vous n'obtenez pas d'erreur d'exécution lorsque la méthode **Append** est appelée sur la collection **Fields** d'un objet **Record** ouvert. Le nouveau champ est ajouté à la collection **Fields** de l'objet **Record**. Si l'objet **Record** est dérivé d'un objet **Recordset**, le nouveau champ n'apparaît pas dans la collection **Fields** de l'objet **Recordset**.

Vous pouvez créer un champ non existant et l'ajouter à la collection **Fields** en affectant une valeur à ce champ comme s'il existait déjà dans la collection. Cette affectation déclenche la création et l'ajout automatiques de l'objet **Field**, puis son exécution effective.

Une fois l'objet **Field** ajouté à la collection **Fields** d'un objet **Record**, appelez la méthode **Update** de la collection **Fields** pour enregistrer cette modification.

