---
title: Notes sur la sécurité XML
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 69672b2993cb91ace5bd447b762f33fcbd66c1bc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868489"
---
# <a name="xml-security-considerations"></a>Notes sur la sécurité XML


**S’applique à**: Access 2013, Office 2013

## <a name="xml-security-considerations"></a>Considérations relatives à la sécurité XML

Les méthodes ADO **Record** et **Open** de l'objet **Recordset** ne peuvent être considérées comme des opérations sûres avec Internet Explorer. Si ces méthodes sont utilisées dans un code de script s'exécutant dans une application ou un contrôle sur un navigateur hôte, la configuration de sécurité du navigateur aura une influence sur son fonctionnement.

Internet Explorer 5 dispose de restrictions de sécurité pour ce type d'opérations par défaut dans les zones Internet. Avec cette configuration, l'objet **Recordset** ne peut pas accéder au système de fichiers local sur le client, ni accéder aux sources de données en dehors du domaine du serveur à partir duquel la page a été téléchargée. Plus précisément, lorsqu'il est exécuté sur un navigateur hôte, un objet **Recordset** ne peut être à nouveau enregistré dans un fichier que s'il se trouve sur le même serveur à partir duquel la page a été téléchargée. De la même façon, vous pouvez ouvrir un objet **Recordset** en le chargeant à partir d'un fichier uniquement si ce dernier réside sur le même serveur à partir duquel la page a été téléchargée.

Pour plus d'informations sur la sécurité avec Internet Explorer, consultez l'article technique "Problèmes de sécurité ADO et RDS dans Microsoft Internet Explorer."

