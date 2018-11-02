---
title: LoadFromFile, méthode (ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 96bc0f55f6524a2aaa04bbe1f9b591ff2eb85bb8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925722"
---
# <a name="loadfromfile-method-ado"></a>LoadFromFile, méthode (ADO)


**S’applique à**: Access 2013, Office 2013



Charge le contenu d'un fichier existant dans un objet [Stream](stream-object-ado.md).

## <a name="syntax"></a>Syntaxe

*Flux de données*. LoadFromFile, *nom de fichier*

## <a name="parameter"></a>Paramètre

  - *FileName*

  - Valeur de type **String** qui contient le nom d'un fichier à charger dans l'objet **Stream**. *Nom de fichier* peut contenir n’importe quel chemin d’accès valide et un nom au format UNC. Si le fichier spécifié n'existe pas, une erreur d'exécution se produit.

## <a name="remarks"></a>Notes

Cette méthode peut être utilisée pour charger le contenu d'un fichier local dans un objet **Stream**. Cela permet de télécharger le contenu d'un fichier local sur un serveur.

L'objet **Stream** doit être déjà ouvert avant d'appeler la méthode **LoadFromFile**. Cette méthode ne modifie pas la liaison de l'objet **Stream**; il sera toujours lié à l'objet spécifié par l'URL ou l'objet **Record** avec lequel l'objet **Stream** a été initialement ouvert.

La méthode **LoadFromFile** remplace le contenu actuel de l'objet **Stream** par les données lues à partir du fichier. Tous les octets présents dans l'objet **Stream** sont remplacés par le contenu du fichier. Tous les octets qui existaient déjà ou restent encore après la création de la propriété [EOS](eos-property-ado.md) par **LoadFromFile** sont tronqués.

Après un appel de la méthode **LoadFromFile**, la position actuelle est définie au début de l’objet **Stream** ([Position](position-property-ado.md) est 0).

Dans la mesure où 2 octets peuvent être ajoutés au début du flux pour des raisons de codage, il se peut que la taille du flux ne corresponde pas exactement à celle du fichier à partir duquel il a été chargé.

