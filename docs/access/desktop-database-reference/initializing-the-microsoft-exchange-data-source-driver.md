---
title: Initialisation du pilote de source de données Microsoft Exchange
TOCTitle: Initializing the Microsoft Exchange Data Source driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 267ea341b9108fb344ecdb59f45a33ae79deef83
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631448"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a>Initialisation du pilote de source de données Microsoft Exchange

**S’applique à** : Access 2013, Office 2013

Lorsque vous installez le pilote de source de données Microsoft Exchange, le programme d’installation écrit un ensemble de valeurs par défaut dans le Registre Microsoft Windows dans les sous-clés Engines et ISAM Formats. Vous ne devez pas modifier ces paramètres directement ; utilisez le programme d’installation de votre application pour ajouter, supprimer ou modifier ces paramètres. Les sections suivantes décrivent l’initialisation et les paramètres de format ISAM pour le pilote de source de données Microsoft Exchange.

## <a name="microsoft-exchange-data-source-initialization-settings"></a>Paramètres d Exchange d’initialisation de la source de données Microsoft

Le **dossier Access Connectivity EngineEngines\\\\ Exchange** inclut les paramètres d’initialisation du pilote Aceexch.dll, utilisé pour l’accès externe aux dossiers Microsoft Outlook et Microsoft Exchange. L'unique entrée dans ce dossier est la suivante :

`win32=<path>\ACEEXCH.DLL`

Le moteur de base de données Microsoft Exchange utilise ce paramètre pour indiquer l'emplacement du pilote Aceexch.dll. Le chemin d'accès complet est déterminé au moment de l'installation. Les valeurs sont de type REGSZ\_.

Le format ISAM du client Outlook et le format ISAM du client Exchange donnent des résultats similaires. La seule différence est que ces deux clients utilisent des noms différents pour les mêmes colonnes. Les deux formats ISAM ont été créés afin que le moteur de base de données Microsoft Access puisse retourner les noms de colonnes dans un style particulier souhaité par l'utilisateur.

## <a name="microsoft-outlook-client-isam-formats"></a>Formats ISAM du client Microsoft Outlook

Le **dossier Access Connectivity EngineISAM\\ Formats\\ Outlook 9.0** contient les entrées suivantes.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom d'entrée</p></th>
<th><p>Type</p></th>
<th><p>Valeur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Moteur</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Outlook()</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.



## <a name="microsoft-exchange-client-isam-formats"></a>Formats ISAM du client Microsoft Exchange

Le **dossier Access Connectivity EngineISAM\\ Formats\\ Exchange 4.0** contient les entrées suivantes.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom d'entrée</p></th>
<th><p>Type</p></th>
<th><p>Valeur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Moteur</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange()</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a>Personnalisation du fichier Schema.ini pour les données Outlook et Exchange données

Le fichier Schema.ini est utilisé par le format ISAM Outlook et le format ISAM Exchange pratiquement de la même manière que par le format ISAM texte. Le fichier Schema.ini contient les paramètres spécifiques d'une source de données : mise en fome des données, noms des colonnes auxquelles accéder.

Il n'est pas nécessaire de modifier le fichier Schema.ini pour pouvoir lire, importer ou exporter des données pour Outlook et Exchange. De nombreux paramètres du fichier Schema.ini pour Outlook et Exchange sont spécifiques à des balises internes requises par MAPI. Vous ne devez pas tenter de modifier les valeurs de ces balises.

