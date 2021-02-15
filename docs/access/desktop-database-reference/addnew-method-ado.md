---
title: AddNew, méthode (ADO)
TOCTitle: AddNew method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f733c574ba7927587c6fcb6305a361ca1070de0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282512"
---
# <a name="addnew-method-ado"></a>AddNew, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Crée un enregistrement pour un objet [Recordset](recordset-object-ado.md) actualisable.

## <a name="syntax"></a>Syntaxe

*recordset*. AddNew *FieldList*, *Values*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*recordset* |Objet **Recordset**.|
|*FieldList* |Facultatif. Nom unique ou tableau de noms ou de positions ordinales des champs dans le nouvel enregistrement.|
|*Values* |Facultatif. Valeur unique ou tableau de valeurs des champs dans le nouvel enregistrement. Si *Fieldlist* est un tableau, *Values* doit aussi être un tableau avec le même nombre de membres, sans quoi, une erreur se produit. L'ordre des noms de champs doit correspondre à celui des valeurs de ces champs dans chaque tableau.|

## <a name="remarks"></a>Remarques

Faites appel à la méthode **AddNew** pour créer et initialiser un enregistrement. Utilisez la méthode [Supports](supports-method-ado.md) avec **adAddNew** (une valeur [CursorOptionEnum](cursoroptionenum.md)) pour vérifier si vous pouvez ajouter des enregistrements à l'objet **Recordset** actif.

Une fois la méthode **AddNew** appelée, le nouvel enregistrement devient l'enregistrement actif et reste actif jusqu'à ce que vous appeliez la méthode [Update](update-method-ado.md). Comme ce nouvel enregistrement est ajouté au **Recordset**, l'appel de **MoveNext** après Update déplace la position actuelle au delà de l'objet **Recordset** et **EOF** prend la valeur True. Si l'objet **Recordset** ne prend pas en charge les signets, vous risquez de ne pas pouvoir accéder au nouvel enregistrement après être passé à un autre enregistrement. Selon le type de curseur que vous utilisez, il vous faudra peut-être appeler la méthode [Requery](requery-method-ado.md) pour rendre le nouvel enregistrement accessible.

Si vous appelez la méthode **AddNew** pendant que vous modifiez l'enregistrement actif ou que vous ajoutez un nouvel enregistrement, ADO appelle la méthode **Update** pour enregistrer les modifications apportées, puis crée l'enregistrement.

Le comportement de la méthode **AddNew** dépend du mode de mise à jour de l'objet **Recordset** et selon que vous passez des arguments *Fieldlist* et *Values*.

En *mode de mise à jour immédiate* (dans lequel le fournisseur écrit les modifications apportées dans la source de données sous-jacente dès que vous appelez la méthode **Update**), l’appel de la méthode **AddNew** sans arguments attribue la valeur **adEditAdd** (une valeur [EditModeEnum](editmodeenum.md)) à la propriété [EditMode](editmode-property-ado.md). Le fournisseur met en cache toutes les modifications locales de valeurs de champ. L’appel de la méthode **Update** publie le nouvel enregistrement dans la base de données et réinitialise la propriété **EditMode** à **adEditNone** (valeur **EditModeEnum**). Si vous passez les arguments *Fieldlist* et *Values*, ADO publie immédiatement le nouvel enregistrement dans la base de données (aucun appel de la méthode **Update** n’est requis) ; la valeur de la propriété **EditMode** reste inchangée (**adEditNone**).

En *mode de mise à jour en lot* (dans lequel le fournisseur met en cache plusieurs modifications et les écrit dans la source de données sous-jacente uniquement lorsque vous appelez la méthode [UpdateBatch](updatebatch-method-ado.md)), l’appel de la méthode **AddNew** sans arguments définit la propriété **EditMode** à **adEditAdd**. Le fournisseur met en cache toutes les modifications locales de valeurs de champ. L’appel de la méthode **Update** ajoute le nouvel enregistrement au **Recordset** actif et réinitialise la propriété **EditMode** à **adEditNone**. Toutefois, le fournisseur publie les modifications dans la base de données sous-jacente uniquement lorsque vous appelez la méthode **UpdateBatch**. Si vous passez les arguments *Fieldlist* et *Values*, ADO envoie le nouvel enregistrement au fournisseur pour qu’il le stocke dans un cache. Vous devez appeler la méthode **UpdateBatch** pour publier le nouvel enregistrement dans la base de données sous-jacente.

