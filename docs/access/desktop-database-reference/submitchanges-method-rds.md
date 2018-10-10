---
title: SubmitChanges, méthode (RDS)
TOCTitle: SubmitChanges Method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3227d6a8f7071ee4cdd95aa73c56d8bf61d9e26e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470761"
---
# <a name="submitchanges-method-rds"></a>SubmitChanges, méthode (RDS)


**S’applique à**: Access 2013 | Office 2013

Envoie les modifications en attente de l'objet [Recordset](recordset-object-ado.md) actualisable et placé dans le cache local à la source de données spécifiée dans la propriété [Connect](connect-property-rds.md) de la propriété [URL](url-property-rds.md).

## <a name="syntax"></a>Syntaxe

*DataControl*. SubmitChanges

*DataFactory*. SubmitChanges*connexion* *jeu d’enregistrements*

## <a name="parameters"></a>Paramètres

  - *DataControl*

  - Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).

  - *DataFactory*

  - Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md).

  - *Connection*

  - Valeur de type **String** représentant la connexion créée avec la propriété **Connect** de l'objet **RDS.DataControl**.

  - *Recordset*

  - Variable objet représentant un objet **Recordset**.

## <a name="remarks"></a>Notes

Les propriétés [Connect](connect-property-rds.md), [Server](server-property-rds.md) et [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) doivent être définies avant de pouvoir utiliser la méthode **SubmitChanges** avec l'objet **RDS.DataControl**.

Si vous appelez la méthode [CancelUpdate](cancelupdate-method-rds.md) après avoir appelé **SubmitChanges** pour le même objet **Recordset**, l'appel **CancelUpdate** échoue car les modifications ont déjà été validées.

Seuls les enregistrements modifiés sont envoyés pour modification. Par ailleurs, soit toutes les modifications aboutissent, soit elles échouent toutes.

Vous pouvez utiliser **SubmitChanges** qu’avec l’objet **RDSServer.DataFactory** *par défaut* . Les objets métier personnalisés ne peuvent pas utiliser cette méthode.

Si la propriété **URL** a été définie, **SubmitChanges** envoie les modifications à l'emplacement indiqué par l'URL.

