---
title: Fields, collection (ADO)
TOCTitle: Fields Collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9d4b710c8e0a9293c9164395cf9bff3078a3b36
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879402"
---
# <a name="fields-collection-ado"></a>Fields, collection (ADO)


**S’applique à**: Access 2013, Office 2013

Contient tous les objets [Field](field-object-ado.md) d'un objet [Recordset](recordset-object-ado.md) ou [Record](record-object-ado.md).

## <a name="remarks"></a>Notes

Un objet **Recordset** possède une collection **Fields** composée d'objets **Field**. Chaque objet **Field** correspond à une colonne du **Recordset**. Vous pouvez remplir la collection **Fields** avant d'ouvrir l'objet **Recordset** en appelant la méthode [Refresh](refresh-method-ado.md) sur cette collection.


> [!NOTE]
> <P>[!REMARQUE] Pour plus d'informations sur l'utilisation des objets <STRONG>Field</STRONG>, voir la rubrique traitant de l'objet <STRONG>Field</STRONG>.</P>



La collection **Fields** possède une méthode [Append](append-method-ado.md), qui crée et ajoute provisoirement un objet **Field** à la collection, ainsi qu'une méthode **Update**, qui finalise les ajouts et les suppressions.

Un objet **Record** possède deux champs spéciaux qui peuvent être indexés avec des constantes [FieldEnum](fieldenum.md). Une constante donnée accède à un champ contenant le flux par défaut de l' **enregistrement**, une autre accède à un champ contenant la chaîne URL absolue de l' **enregistrement**.

Certains fournisseurs (par exemple, [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md)) peuvent remplir la collection **Fields** avec un sous-ensemble de champs disponibles pour l'objet **Record** ou **Recordset**. D'autres champs ne seront pas ajoutés à la collection tant qu'ils n'auront pas été référencés par leur nom ou indexés par votre code.

Si vous essayez de référencer un champ inexistant par son nom, un nouvel objet **Field** sera ajouté à la collection **Fields** avec une propriété [Status](status-property-ado-field.md) définie sur **adFieldPendingInsert**. Lorsque vous appelez [Update](update-method-ado.md), ADO crée un nouveau champ dans votre source de données si cela est autorisé par votre fournisseur.

