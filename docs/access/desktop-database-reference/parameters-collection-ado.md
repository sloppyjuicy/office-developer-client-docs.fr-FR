---
title: Parameters, collection (ADO)
TOCTitle: Parameters Collection (ADO)
ms:assetid: 554387c3-3572-5391-3b24-c7d3443844cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249283(v=office.15)
ms:contentKeyID: 48544923
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7a1da73679bd63de0c35362b87b2db8259698614
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867789"
---
# <a name="parameters-collection-ado"></a>Parameters, collection (ADO)


**S’applique à**: Access 2013, Office 2013

Contient tous les objets [Parameter](parameter-object-ado.md) d'un objet [Command](command-object-ado.md).

## <a name="remarks"></a>Notes

Un objet **Command** possède une collection **Parameters** composée d'objets **Parameter**.

L'utilisation de la méthode [Refresh](refresh-method-ado.md) sur une collection **Parameters** de l'objet **Command** récupère les informations des paramètres du fournisseur pour la procédure stockée ou la requête paramétrée spécifiée dans l'objet **Command**. Certains fournisseurs ne prennent pas en charge les appels de procédure stockée ou les requêtes paramétrées ; si vous appelez la méthode **Refresh** sur la collection **Parameters** avec ce type de fournisseur, vous obtenez une erreur.

Si vous n'avez pas défini vos propres objets **Parameter** et que vous accédez à la collection **Parameters** avant d'appeler la méthode **Refresh**, ADO appelle automatiquement la méthode et remplit la collection à votre place.

Si vous connaissez les propriétés des paramètres associés à la procédure stockée ou à la requête paramétrée que vous voulez appeler, vous pouvez minimiser les appels au fournisseur pour accroître les performances. Utilisez la méthode [CreateParameter](createparameter-method-ado.md) pour créer des objets **Parameter** avec les paramètres de propriété appropriés et utilisez la méthode [Append](append-method-ado.md) pour les ajouter à la collection **Parameters**. Cela vous permet de définir et de renvoyer des valeurs de paramètre sans appeler le fournisseur afin qu'il fournisse les informations de paramètre. Si vous écrivez du code pour un fournisseur qui ne fournit pas d'informations de paramètre, vous devez remplir manuellement la collection **Parameters** à l'aide de cette méthode pour pouvoir utiliser des paramètres. Utilisez la méthode [Delete](delete-method-ado-parameters-collection.md) pour supprimer les objets **Parameter** de la collection **Parameters** si nécessaire.

Les objets de la collection **Parameters** d'un objet **Recordset** sont hors de portée (ils deviennent donc indisponibles) lorsque cet objet **Recordset** est fermé.

