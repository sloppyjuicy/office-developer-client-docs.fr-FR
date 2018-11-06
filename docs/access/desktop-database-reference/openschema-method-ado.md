---
title: OpenSchema, méthode (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9e7fb19504e606fed9960a3982c0f98f9081325
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997560"
---
# <a name="openschema-method-ado"></a>OpenSchema, méthode (ADO)

**S’applique à**: Access 2013, Office 2013

Obtient du fournisseur les informations du schéma de base de données.

## <a name="syntax"></a>Syntaxe

**Définir *** recordset* = *connexion*. OpenSchema (* QueryType *, *critères*, *IDSchéma doit être utilisé*)

## <a name="return-values"></a>Valeurs de retour

Retourne un objet [Recordset](recordset-object-ado.md) qui contient les informations de schéma. L'objet **Recordset** est ouvert en tant que curseur statique, en lecture seule. Le *QueryType* détermine les colonnes qui apparaissent dans le **jeu d’enregistrements**.

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*QueryType* |Valeur [SchemaEnum](schemaenum.md) qui représente le type de requête de schéma à exécuter.|
|*Critères* |Facultatif. Tableau de contraintes de requête pour chaque option *QueryType* , répertoriée dans **SchemaEnum**.|
|*Si IDSchéma* |GUID d'une requête d'un schéma de fournisseur non définie par la spécification OLE DB. Ce paramètre est requis si *QueryType* a la valeur **adSchemaProviderSpecific**; dans le cas contraire, il n’est pas utilisé.|

## <a name="remarks"></a>Notes

La méthode **OpenSchema** renvoie des informations autodescriptives sur la source de données, telles que les tables figurant dans la source de données, les colonnes des tables et les type de données pris en charge.

L’argument *QueryType* est un GUID qui indique les colonnes (schémas) retournés. La spécification OLE DB comporte une liste complète de schémas.

L'argument *Critères* limite les résultats d'une requête de schéma. *Critères* spécifie un tableau de valeurs qui doivent apparaître dans un sous-ensemble correspondant de colonnes, appelées *colonnes de contraintes* dans l'objet **Recordset** résultant.

La constante **adSchemaProviderSpecific** est utilisée pour l’argument *QueryType* si le fournisseur définit ses propres requêtes de schéma non standard en dehors de celles répertoriées ci-dessus. Lorsque cette constante est utilisée, l’argument *IDSchéma doit être utilisé* est requise pour transmettre le GUID de la requête de schéma à exécuter. Si *QueryType* a la valeur **adSchemaProviderSpecific** mais *si IDSchéma* n’est pas spécifié, une erreur se produit.

Les fournisseurs ne doivent pas obligatoirement prendre en charge toutes les requêtes de schéma standard OLE DB. En fait, seules les requêtes **adSchemaTables**, **adSchemaColumns** et **adSchemaProviderTypes** sont requises par la spécification OLE DB. Toutefois, le fournisseur n’est pas requis pour prendre en charge les contraintes de *critères* ci-dessus pour ces requêtes de schéma.

**L’utilisation du Service de données à distance** La méthode **OpenSchema** n’est pas disponible sur un objet de [connexion](connection-object-ado.md) côté client.

> [!NOTE]
> Dans Visual Basic, les colonnes qui possèdent un entier non signé de quatre octets (DBTYPE UI4) dans l'objet **Recordset** retourné par la méthode **OpenSchema** de l'objet **Connection** ne peuvent pas être comparées à d'autres variables. Pour plus d'informations sur les types de données OLE DB, consultez le chapitre 13 et l'Annexe A du *Guide de référence du programmeur Microsoft OLE DB*.


