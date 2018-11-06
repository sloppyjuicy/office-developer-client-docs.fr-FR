---
title: Propriété Relation.PartialReplica (DAO)
TOCTitle: PartialReplica Property
ms:assetid: 3cb15639-371e-06e3-e2ba-30466ce09a72
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192692(v=office.15)
ms:contentKeyID: 48544324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053557
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 11f8017c01cec9af2da26bedaf689d69554e554c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998186"
---
# <a name="relationpartialreplica-property-dao"></a>Propriété Relation.PartialReplica (DAO)

**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur sur une **Relation** indiquant si cette relation doit être prise en compte lors du remplissage d'un réplica partiel à partir d'un réplica complet. (Bases de données de moteur de base de données Microsoft Access uniquement). Type de données **Boolean** en lecture/écriture.

## <a name="syntax"></a>Syntaxe

*expression* . PartialReplica

*expression* Expression qui renvoie un objet **Relation** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est une donnée de type booléen qui est **True** lorsque la relation doit être prise en compte lors de la synchronisation.

Cette propriété vous permet de répliquer des données d'un réplica complet dans un réplica partiel en fonction des relations entre les tables. Vous pouvez utiliser la propriété **PartialReplica** lorsque la propriété **ReplicaFilter** seule ne suffit pas à spécifier avec précision les données à repliquer dans le réplica partiel. Supposez par exemple que vous avez une base de données dont la table Customers a une relation un-à-plusieurs avec la table Orders et que vous voulez configurer un réplica partiel qui réplique uniquement les commandes des clients de la région Californie (plutôt que toutes les commandes). Vous ne pouvez pas définir la propriété **ReplicaFilter** au niveau de la table Orders sur Region = 'CA' car le champ Region se trouve dans la table Customers, et non dans la table Orders.

Pour répliquer toutes les commandes de la région Californie, vous devez indiquer que la relation entre les tables Orders et Customers sera active lors de la réplication. Une fois le réplica partiel créé, les étapes suivantes le renseignent avec toutes les commandes de la région Californie :

1.  Définir la propriété **ReplicaFilter** sur l’objet Customers **TableDef** à « Region = 'CA' ».

2.  Définissez la valeur de la propriété **PartialReplica** sur **True** au niveau de l'objet **Relation** correspondant à la relation entre les tables Orders et Customers.

3.  Invoquez la méthode **PopulatePartial**.
    

> [!NOTE]
> [!REMARQUE] Lorsque vous définissez un filtre ou une relation de réplica, notez que les enregistrements du réplica partiel ne répondant pas aux critères de restriction seront supprimés du réplica partiel mais pas du réplica complet. Par exemple, supposons que vous définissez la propriété **ReplicaFilter** sur les clients **TableDef** dans le réplica partiel à « Region = 'CA' » et vous puis remplir la base de données. Cette opération va entraîner l'ajout ou la mise à jour de tous les enregistrements relatifs aux clients basés en Californie. 
> 
> Si vous rétablissez la propriété **ReplicaFilter** pour « Region = 'FL' » et remplir la base de données, tous les enregistrements de la région Californie du réplica partiel seront supprimées et tous les enregistrements de Floride seront insérées à partir du réplica complet. Aucun enregistrement du réplica complet n'est supprimé. 
>
> Avant de définir la propriété **ReplicaFilter** ou **PartialReplica**, il convient de synchroniser le réplica partiel dans lequel vous définissez ces propriétés avec le réplica complet. Vous garantissez ainsi que les modifications en cours du réplica partiel sont fusionnées dans ce dernier avant que tout enregistrement ne soit supprimé.


