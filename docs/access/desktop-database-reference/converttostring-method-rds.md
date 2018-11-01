---
title: ConvertToString, méthode (RDS)
TOCTitle: ConvertToString Method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0820aec3ce8606f5f8f0fcb8dac838ae7bbd15d8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869127"
---
# <a name="converttostring-method-rds"></a>ConvertToString, méthode (RDS)


**S’applique à**: Access 2013, Office 2013 

Convertit un objet [Recordset](recordset-object-ado.md) en chaîne MIME qui représente les données du jeu d'enregistrements.

## <a name="syntax"></a>Syntaxe

*DataFactory*. ConvertToString (*jeu d’enregistrements*)

## <a name="parameters"></a>Paramètres

  - *DataFactory*

  - Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md).

  - *Recordset*

  - Variable objet représentant un objet **Recordset**.

## <a name="remarks"></a>Notes

Avec des fichiers .asp, utilisez **ConvertToString** pour incorporer l'objet **Recordset** dans une page HTML générée sur le serveur afin de le transporter sur un ordinateur client.

**ConvertToString** commence par charger l'objet **Recordset** dans les tables du service de curseur, puis génère un flux au format MIME.

Sur le client, RDS (Remote Data Service) peut reconvertir la chaîne MIME en un objet **Recordset** parfaitement fonctionnel. Cette méthode fonctionne bien pour gérer moins de 400 lignes de données comportant moins de 1024 octets par ligne, mais il faut l'éviter si vous voulez diffuser en continu des données BLOB et des jeux de résultats volumineux via HTTP. En effet, la chaîne n'est pas compressée et le transport, via HTTP, d'ensembles importants de données prend un temps considérable comparé au format de transmission Tablegram optimisé, défini et déployé par RDS (Remote Data Service) en tant que format de protocole de transport natif.


> [!NOTE]
> [!REMARQUE] Si vous utilisez des pages ASP pour incorporer la chaîne MIME résultante dans une page HTML cliente, sachez que les versions de VBScript antérieures à 2.0 limitent la taille de la chaîne à 32 Ko. Si cette limite est dépassée, une erreur est retournée. Par conséquent, essayez de limiter la portée de la requête lorsque vous procédez à une incorporation MIME via des fichiers .asp. Pour résoudre ce problème, téléchargez la dernière version de VBScript à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/downloads/en/default.aspx).


