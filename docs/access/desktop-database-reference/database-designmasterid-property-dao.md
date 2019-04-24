---
title: Propriété Database. DesignMasterID (DAO)
TOCTitle: DesignMasterID Property
ms:assetid: c0545561-d44f-5479-8ae0-e3955db91761
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822824(v=office.15)
ms:contentKeyID: 48547508
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a189d16880fccdc34c169aee61c6781e1d86afa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294931"
---
# <a name="databasedesignmasterid-property-dao"></a>Propriété Database. DesignMasterID (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur de 16 octets qui identifie de façon unique le réplica-maître d’un jeu de réplicas (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . DesignMasterID

*expression* Variable qui représente un objet **Database** .

## <a name="remarks"></a>Remarques

Vous ne devez définir la propriété **DesignMasterID** que si vous souhaitez déplacer le réplica-maître actif. Si vous définissez cette propriété, un réplica spécifique du jeu de réplicas devient le réplica-maître.

> [!NOTE]
> [!REMARQUE] Ne créez jamais de deuxième réplica-maître dans un jeu de réplicas, car sa présence peut entraîner la perte de données.

Dans des cas extrêmes (effacement ou endommagement du réplica-maître, par exemple), vous pouvez définir cette propriété sur le réplica actif. Toutefois, si vous la définissez sur un réplica alors que le jeu contient déjà un autre réplica-maître, vous risquez de fractionner le jeu de réplicas en deux jeux incompatibles et d'empêcher toute synchronisation ultérieure des données.

Si vous définissez un réplica comme nouveau réplica-maître du jeu, synchronisez-le avec tous les réplicas du jeu de réplicas avant de définir la propriété **DesignMasterID** du réplica. Dans ce cadre, le réplica doit être ouvert en mode exclusif.

Si vous définissez un réplica en lecture seule comme réplica-maître, le réplica cible est en lecture/écriture. L'ancien réplica-maître reste également en lecture/écriture.

Le paramètre de la propriété **DesignMasterID** est enregistré dans la table système MSysRepInfo.

## <a name="example"></a>Exemple

L'exemple ci-dessous définit la propriété **DesignMasterID** sur le paramètre de propriété **ReplicaID** d'une autre base de données, qui devient alors le réplica-maître du jeu de réplicas. L'ancien réplica-maître et le nouveau sont synchronisés afin de répercuter la modification de la structure. Pour que ce code puisse fonctionner, vous devez créer un réplica-maître et un réplica, inclure leur nom et leur chemin d'accès, puis exécuter ce code à partir d'une autre base de données que l'ancien réplica-maître ou le nouveau.

```vb 
 Sub SetNewDesignMaster(strOldDM as String, _ 
    strNewDM as String) 
    
    Dim dbsOld As Database 
    Dim dbsNew As Database 
    
    ' Open the current Design Master in exclusive mode. 
    Set dbsOld = OpenDatabase(strOldDM, True) 
    
    ' Open the database that will become the new 
    ' Design Master. 
    Set dbsNew = OpenDatabase(strNewDM) 
    
    ' Make the new database the Design Master. 
    dbsOld.DesignMasterID = dbsNew.ReplicaID 
    
    ' Synchronize the old Design Master with the new 
    ' Design Master, and allow two-way exchanges. 
    dbsOld.Synchronize strNewDM, dbRepImpExpChanges 
    dbsOld.Close 
    dbsNew.Close 
 
 End Sub 
 
```

