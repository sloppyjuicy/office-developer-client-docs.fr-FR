---
title: OpenSchema, méthode (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ca69b9d761629d42138780517f8de806ed7e8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288335"
---
# <a name="openschema-method-ado"></a>OpenSchema, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Obtient du fournisseur les informations du schéma de base de données.

## <a name="syntax"></a>Syntaxe

**Set * ** = **connexion*Recordset. OpenSchema (* QueryType *, *Criteria*, *SchemaID*)

## <a name="return-values"></a>Valeurs de retour

Retourne un objet [Recordset](recordset-object-ado.md) qui contient les informations de schéma. L'objet **Recordset** est ouvert en tant que curseur statique, en lecture seule. Le paramètre *TypeRequête* détermine les colonnes qui apparaîtront dans l’objet **Recordset**.

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*QueryType* |Valeur [SchemaEnum](schemaenum.md) qui représente le type de requête de schéma à exécuter.|
|*Critères* |Facultatif. Tableau de contraintes de requête pour chaque option *TypeRequête*, répertoriée dans **SchemaEnum**.|
|*SchemaID* |GUID d'une requête d'un schéma de fournisseur non définie par la spécification OLE DB. Ce paramètre est obligatoire si *TypeRequête* a la valeur **adSchemaProviderSpecific** ; sinon, il n'est pas utilisé.|

## <a name="remarks"></a>Remarques

La méthode **OpenSchema ** renvoie des informations autodescriptives sur la source de données, telles que les tables figurant dans la source de données, les colonnes des tables et les type de données pris en charge.

L'argument *TypeRequête* est un GUID qui indique les colonnes (schémas) retournés. La spécification OLE DB comporte une liste complète de schémas.

L'argument *Critères* limite les résultats d'une requête de schéma. *Critères* spécifie un tableau de valeurs qui doivent apparaître dans un sous-ensemble correspondant de colonnes, appelées *colonnes de contraintes* dans l'objet **Recordset** résultant.

La constante **adSchemaProviderSpecific** est utilisée comme argument *TypeRequête* si le fournisseur définit ses propres requêtes de schéma non standard, autres que celles répertoriées ci-dessus. Lorsque cette constante est utilisée, l'argument *IDSchéma* doit être utilisé pour passer le GUID de la requête de schéma à exécuter. Si *TypeRequête* a la valeur **adSchemaProviderSpecific** mais si *IDSchéma* n'est pas spécifié, une erreur se produit.

Les fournisseurs ne doivent pas obligatoirement prendre en charge toutes les requêtes de schéma standard OLE DB. En fait, seules les requêtes **adSchemaTables**, **adSchemaColumns** et **adSchemaProviderTypes** sont requises par la spécification OLE DB. Le fournisseur ne doit pas non plus nécessairement prendre en charge les contraintes de l'argument *Critères* répertoriées ci-dessus pour ces requêtes de schéma.

**Utilisation des services de données à distance** La méthode **OpenSchema** n'est pas disponible pour un objet [Connection](connection-object-ado.md) côté client.

> [!NOTE]
> Dans Visual Basic, les colonnes qui possèdent un entier non signé de quatre octets (DBTYPE UI4) dans l'objet **Recordset** retourné par la méthode **OpenSchema** de l'objet **Connection** ne peuvent pas être comparées à d'autres variables. Pour plus d'informations sur les types de données OLE DB, consultez le chapitre 13 et l'Annexe A du *Guide de référence du programmeur Microsoft OLE DB*.


