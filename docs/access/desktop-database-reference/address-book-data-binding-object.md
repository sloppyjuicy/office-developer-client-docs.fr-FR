---
title: Objet de liaison de données du carnet d’adresses
TOCTitle: Address Book Data-Binding object
ms:assetid: cf43f645-1ee1-8655-eb70-86d601e9f3f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250030(v=office.15)
ms:contentKeyID: 48547807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 25219515f5a650cbeffbe959a5a0628764a160f8
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558627"
---
# <a name="address-book-data-binding-object"></a>Objet de liaison de données du carnet d’adresses

**S’applique à** : Access 2013, Office 2013

L'application Carnet d'adresses utilise l'objet [RDS.DataControl](datacontrol-object-rds.md) pour lier les données de la base de données SQL Server à un objet visuel (dans le cas présent, un tableau DHTML) dans la page HTML cliente de l'application. La logique de programmation événementielle de VBScript utilise l'objet [RDS.DataControl](datacontrol-object-rds.md) pour :

  - interroger la base de données, lui envoyer des mises à jour et actualiser la grille de données ;

  - autoriser des utilisateurs à accéder au premier ou dernier enregistrement ainsi qu'à l'enregistrement suivant ou précédent de la grille de données.

L'exemple de code suivant définit le composant **RDS.DataControl**:

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

La balise OBJECT définit le composant **RDS.DataControl** dans le programme. Elle inclut deux types de paramètres :

  - ceux associés à la balise OBJECT générique ;

  - ceux propres à l'objet **RDS.DataControl**.

## <a name="generic-object-tag-parameters"></a>Paramètres de la balise OBJECT générique

Le tableau suivant décrit les paramètres associés à la balise OBJECT.

|**Paramètre**|**Description**|
|:------------|:--------------|
|**_CLASSID_**|Nombre 128 bits unique qui permet au système d’identifier le type d’objet incorporé. Cet identificateur est conservé dans le Registre système de l’ordinateur local. (Pour les ID de classe du **RDS. Objet DataControl** , voir [RDS. DataControl, objet](/office/client-developer/access/desktop-database-reference/datacontrol-object-rds.md). |
|**_ID_**     |Définit un identificateur de niveau document permettant d'identifier l'objet incorporé dans le code.  |

## <a name="rdsdatacontrol-tag-parameters"></a>Paramètres de la balise RDS.DataControl

Le tableau suivant décrit les paramètres spécifiques à l’objet **RDS.DataControl**. (Pour obtenir une liste complète des paramètres de l’objet **RDS.DataControl** et savoir quand les implémenter, consultez [RDS.DataControl, objet](datacontrol-object-rds.md)).

|**Paramètre**|**Description**|
|:------------|:--------------|
|[SERVEUR](/office/client-developer/access/desktop-database-reference/server-property-rds.md)| Si vous utilisez HTTP, la valeur est le nom de l’ordinateur serveur précédé de https:// </br>|
|[CONNECT](/office/client-developer/access/desktop-database-reference/connect-property-rds.md)| Fournit les informations de connexion nécessaires pour la connexion de l'objet <strong>RDS.DataControl</strong> à SQL Server. </br>|
|[SQL](/office/vba/access/concepts/miscellaneous/sql-property-ado.md)| Définit ou renvoie la chaîne de requête utilisée pour récupérer [l’recordset](/office/client-developer/access/desktop-database-reference/recordset-object-ado.md)|
