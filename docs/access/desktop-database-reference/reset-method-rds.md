---
title: Reset, méthode (RDS - référence du bureau de la base de données Access)
TOCTitle: Reset Method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab88aefabca73b9c2b23a4cf66664aa892310cdc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884484"
---
# <a name="reset-method-rds"></a>Reset, méthode (RDS)


**S’applique à**: Access 2013, Office 2013

Applique un tri ou un filtre à un objet **Recordset** côté client en fonction des propriétés de tri et de filtre spécifiées.

## <a name="syntax"></a>Syntaxe

*DataControl*. Réinitialisation (*valeur*)

## <a name="parameters"></a>Paramètres

  - *DataControl*

  - Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).

  - *valeur*

  - Facultatif. Valeur de type **Boolean**. Si la valeur est **True** (par défaut), cela permet d'effectuer un filtrage sur l'ensemble de lignes « filtré » actuel. Si la valeur est **False**, le filtrage porte sur l'ensemble de lignes d'origine, supprimant toutes les options de filtre précédentes.

## <a name="remarks"></a>Notes

Les propriétés [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) et [FilterColumn](filtercolumn-property-rds.md) fournissent des fonctionnalités de tri et de filtrage pour le cache côté client. La fonctionnalité de tri classe les enregistrements en fonction des valeurs d'une seule colonne. La fonctionnalité de filtre affiche un sous-ensemble d'enregistrements en fonction de certains critères de recherche définis alors que l'objet [Recordset](recordset-object-ado.md) complet est conservé dans le cache. La méthode **Reset** exécute les critères et remplace l'objet **Recordset** actif par un objet **Recordset** qui peut être mis à jour.

Si des modifications apportées aux données d'origine n'ont pas encore été soumises, la méthode **Reset** échoue. Avant tout, utilisez la méthode [SubmitChanges](submitchanges-method-rds.md) pour enregistrer les éventuelles modifications dans un objet **Recordset** en lecture/écriture puis employez la méthode **Reset** pour trier ou filtrer les enregistrements.

Si vous souhaitez effectuer plusieurs filtres sur votre ensemble de lignes, vous pouvez utiliser l’option argument *Boolean* avec la méthode **Reset** . L'exemple suivant montre comment procéder :

