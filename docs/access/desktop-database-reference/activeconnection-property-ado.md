---
title: ActiveConnection, propriété (ADO)
TOCTitle: ActiveConnection property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 10/17/2018
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 2436d1f06c673814cef1b6134f17b1eca2a5763b
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893773"
---
# <a name="activeconnection-property-ado"></a>ActiveConnection, propriété (ADO)

**S’applique à** : Access 2013, Office 2013

Indique l'objet [Connection](connection-object-ado.md) auquel l'objet [Command](command-object-ado.md), [Recordset](recordset-object-ado.md) ou [Record](record-object-ado.md) spécifié appartient actuellement.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **String** contenant la définition d'une connexion si la connexion est fermée, ou une valeur **Variant** contenant l'objet **Connection** actif si la connexion est ouverte. La valeur par défaut est une référence d'objet Null. Reportez-vous à la propriété [ConnectionString](connectionstring-property-ado.md).

## <a name="remarks"></a>Remarques

Utilisez la propriété **ActiveConnection** pour déterminer l'objet **Connection** sur lequel l'objet **Command** est exécuté ou sur lequel l'objet **Recordset** spécifié est ouvert.

### <a name="command"></a>Commande

Pour les objets **Command**, la propriété **ActiveConnection** est en lecture/écriture.

Si vous tentez d'appeler la méthode [Execute](/office/vba/access/concepts/miscellaneous/execute-method-ado-command) sur un objet **Command** avant d'affecter à cette propriété un objet **Connection** ouvert ou une chaîne de connexion valide, une erreur se produit.

**Microsoft Visual Basic** : la définition de la propriété **ActiveConnection** sur *Nothing* dissocie l’objet **Command** de la **connexion** actuelle et entraîne la libération par le fournisseur des ressources associées sur la source de données. Vous pouvez alors associer l’objet **Command** au même objet **Connection** ou à un autre. Certains fournisseurs permettent de remplacer l’objet **Connection** défini dans la propriété par un autre, sans devoir préalablement affecter à la propriété la valeur *Nothing*.

Si la collection [Parameters](parameters-collection-ado.md) de l’objet **Command** contient les paramètres fournis par le fournisseur, le contenu de la collection est effacé si vous attribuez à la propriété **ActiveConnection** la valeur *Nothing* ou un autre objet **Connection**. Si vous créez manuellement des objets [Parameter](parameter-object-ado.md) et que vous les utilisez pour remplir la collection **Parameters** de l’objet **Command**, l’affectation de la valeur *Nothing* ou d’un autre objet **Connection** à la propriété **ActiveConnection** ne modifie pas la collection **Parameters**.

La fermeture de l'objet **Connection** auquel est associé un objet **Command** affecte à la propriété **ActiveConnection** la valeur *Nothing*. L'attribution d'un objet **Connection** fermé à cette propriété génère une erreur.

### <a name="recordset"></a>Recordset

Pour les objets **Recordset** ouverts ou pour les objets **Recordset** dont la propriété [Source](source-property-ado-recordset.md) a pour valeur un objet **Command** valide, la propriété **ActiveConnection** est en lecture seule. Autrement, elle est en lecture/écriture.

Vous pouvez affecter à cette propriété un objet **Connection** valide ou une chaîne de connexion valide. Dans ce cas, le fournisseur crée un objet **Connection** à l'aide de cette définition et ouvre la connexion. De plus, le fournisseur peut définir cette propriété sur le nouvel objet **Connection** pour vous permettre d'accéder à l'objet **Connection** et obtenir des informations complémentaires relatives à l'objet ou exécuter d'autres commandes.

Si vous utilisez l’argument *ActiveConnection* de la méthode [Open](open-method-ado-recordset.md) pour ouvrir un objet **Recordset**, la propriété **ActiveConnection** hérite de la valeur de l’argument.

Si vous affectez à la propriété **Source** de l'objet **Recordset** une variable d'objet **Command** valide, la propriété **ActiveConnection** de l'objet **Recordset** hérite du paramètre de la propriété **ActiveConnection** de l'objet **Command**.

**Utilisation du service de données distante** : lorsqu’elle est utilisée sur un objet Recordset côté client, cette propriété peut être définie uniquement sur une chaîne de connexion ou (dans Microsoft Visual Basic ou Visual Basic, Édition de script) sur *Nothing*.

### <a name="record"></a>Record

Cette propriété est en lecture/écriture lorsque l'objet **Record** est fermé et peut contenir une chaîne de connexion ou une référence à un objet **Connection** ouvert. Cette propriété est en lecture seule lorsque l'objet **Record** est ouvert et qu'il contient une référence à un objet **Connection** ouvert.

Un objet **Connection** est créé implicitement lorsque l'objet **Record** est ouvert à partir d'une URL. Ouvrez l'objet **Record** à l'aide d'un objet **Connection** existant ouvert en affectant à cette propriété l'objet **Connection** ou en utilisant l'objet **Connection** comme paramètre dans l'appel de la méthode [Open](open-method-ado-record.md). Si **l’enregistrement** est ouvert à partir d’un **enregistrement** ou d’un [recordset](recordset-object-ado.md) existant, il est automatiquement associé à l’objet **Connection** de cet objet **Record** ou **Recordset**.

> [!NOTE]
> Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, consultez [LES URL absolues et relatives](absolute-and-relative-urls.md).
