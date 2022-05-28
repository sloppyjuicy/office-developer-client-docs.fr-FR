---
title: 'Annexe A : Fournisseurs'
TOCTitle: 'Appendix A: Providers'
ms:assetid: b3f92279-8d66-ad59-71c4-c0448168125a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249857(v=office.15)
ms:contentKeyID: 48547207
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d7e5706c7603d766f5858f76463aa3b24fab95e2
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769472"
---
# <a name="appendix-a-providers"></a>Annexe A : Fournisseurs


**S’applique à** : Access 2013, Office 2013


Cette section s'intéresse à trois types de fournisseurs : les fournisseurs de données, les fournisseurs de services et les composants de services. Il existe deux catégories de fournisseurs : les fournisseurs de données et les fournisseurs de services. Un *fournisseur de données* est propriétaire de ses données et les expose sous forme de tableaux dans votre application. Un *fournisseur de services* encapsule un service en produisant et en utilisant des données pour enrichir les fonctionnalités de vos applications ADO. Il peut entrer également dans la sous-catégorie des *composants de services* s'il doit fonctionner conjointement avec d'autres fournisseurs ou composants de services.

## <a name="data-providers"></a>Fournisseurs de données

ADO est un outil puissant et flexible capable de se connecter à n'importe quel fournisseur de données d'un groupe de fournisseurs différents tout en continuant d'exposer le même modèle de programmation, indépendamment des fonctionnalités spécifiques du fournisseur choisi.

Cependant, comme chaque fournisseur de données est unique, le mode d'interaction de votre application avec ADO variera légèrement en fonction du fournisseur de données. Les différences portent généralement sur trois grands points :

- Paramètres de connexion dans la propriété [ConnectionString](connectionstring-property-ado.md).

- Utilisation de l'objet [Command](command-object-ado.md).

- Comportement de l'objet [Recordset](recordset-object-ado.md) spécifique au fournisseur.

Les détails concernant chaque fournisseur de données de Microsoft actuellement disponible sont répertoriés ci-dessous.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Zone</p></th>
<th><p>Rubrique</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Bases de données ODBC</p></td>
<td><p><a href="microsoft-ole-db-provider-for-odbc.md">Fournisseur Microsoft OLE DB pour ODBC</a></p></td>
</tr>
<tr class="even">
<td><p>Service d'indexation Microsoft</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Fournisseur Microsoft OLE DB pour le service d’indexation Microsoft</a></p></td>
</tr>
<tr class="odd">
<td><p>Service Microsoft Active Directory</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Fournisseur Microsoft OLE DB pour le service Microsoft Active Directory</a></p></td>
</tr>
<tr class="even">
<td><p>Bases de données Microsoft Jet</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Microsoft OLE DB Provider for Microsoft Jet</a></p></td>
</tr>
<tr class="odd">
<td><p>Microsoft SQL Server</p></td>
<td><p><a href="microsoft-ole-db-provider-for-sql-server.md">Fournisseur Microsoft OLE DB pour SQL Server</a></p></td>
</tr>
<tr class="even">
<td><p>Bases de données Oracle</p></td>
<td><p><a href="microsoft-ole-db-provider-for-oracle.md">Fournisseur Microsoft OLE DB pour Oracle</a></p></td>
</tr>
<tr class="odd">
<td><p>Publication Internet</p></td>
<td><p><a href="microsoft-ole-db-provider-for-internet-publishing.md">Fournisseur Microsoft OLE DB pour la publication Internet</a></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a>Propriétés dynamiques spécifiques au fournisseur

Les collections [Properties](properties-collection-ado.md) des objets [Connection](connection-object-ado.md), [Command](command-object-ado.md) et [Recordset](recordset-object-ado.md) incluent des propriétés dynamiques spécifiques au fournisseur. Ces propriétés donnent des informations sur les fonctionnalités spécifiques au fournisseur qui viennent compléter les propriétés intégrées prises en charge par ADO.

Après avoir établi la connexion et après avoir créé ces objets, utilisez la méthode [Refresh](refresh-method-ado.md) sur la collection **Properties** de l'objet pour obtenir les propriétés spécifiques au fournisseur. Consultez la documentation de fournisseur et le guide OLE DB Programmer's Reference (en anglais) pour obtenir des informations détaillées sur ces propriétés dynamiques.

## <a name="service-providers"></a>Fournisseurs de services

Pour utiliser un fournisseur de services, vous devez fournir un mot clé. Vous devez aussi connaître les propriétés dynamiques spécifiques à chaque fournisseur de services. Les détails spécifiques à chaque fournisseur sont répertoriés pour tous les fournisseurs de services Microsoft disponibles :

- [Microsoft Data Shaping Service pour OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

- [Fournisseur de persistance Microsoft OLE DB](microsoft-ole-db-persistence-provider-ado-service-provider.md)

- [Fournisseur Microsoft OLE DB d'accès à distance](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a>Composants de service

Le composant de services [Service de curseur pour OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) complète les fonctions de prise en charge du curseur des fournisseurs de données. Il exige également l'utilisation d'un mot clé et possède des propriétés dynamiques.

Pour plus d'informations sur les fournisseurs, consultez la documentation relative à Microsoft OLE DB dans le kit de développement logiciel (SDK) des composants Microsoft Data Access ou visitez le [Centre Accès aux Données et Stockage](/sql/connect/sql-data-developer?view=sql-server-2017&preserve-view=true).

## <a name="provider-commands"></a>Commandes du fournisseur

Pour chaque fournisseur répertorié ici, si vos applications permettent aux utilisateurs d’entrer SQL instructions en tant que commandes du fournisseur, vous devez toujours valider l’entrée utilisateur et être vigilant contre les attaques de pirates potentiellement dangereuses à l’aide d’une instruction SQL potentiellement dangereuse, telle que, dans le cadre de l’entrée utilisateur.

