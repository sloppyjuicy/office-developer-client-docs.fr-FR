---
title: Sécurisation des applications RDS
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a531c01750117ae7abbf87e5ba4cb23daf37851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308777"
---
# <a name="securing-rds-applications"></a>Sécurisation des applications RDS

**S’applique à** : Access 2013, Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Problèmes de sécurité dans Microsoft Internet Explorer

Avec les nouvelles améliorations de sécurité ajoutées à Microsoft Internet Explorer, certains objets ADO et RDS sont limités à un environnement de mode «sans échec». Vous devez avoir connaissance de ces problèmes, notamment de ceux liés aux différentes zones, aux niveaux de sécurité, au comportement restrictif, aux opérations potentiellement dangereuses et aux paramètres de sécurité personnalisés.

Pour plus d'informations sur ces problèmes, consultez l'article consacré aux problèmes de sécurité ADO et RDS dans Microsoft Internet Explorer dans les articles techniques ADO (ActiveX Data Objects).

## <a name="security-and-your-web-server"></a>Sécurité et votre serveur Web

Si vous utilisez l'objet [RDSServer. DataFactory](datafactory-object-rdsserver.md) sur votre serveur Web Internet, n'oubliez pas que cela crée un risque de sécurité potentiel. Les utilisateurs externes qui obtiennent un nom de source de données (DSN), un ID utilisateur et un mot de passe valides sont en mesure d'écrire des pages pour envoyer une requête à cette source de données. Si vous souhaitez un accès plus limité à une source de données, une solution possible consiste à annuler l'enregistrement de l'objet **RDSServer.DataFactory** (msadcf.dll) et à le supprimer pour utiliser des objets métier personnalisés avec des requêtes codées en dur.

Pour plus d'informations sur les implications en matière de sécurité de l'utilisation de l'objet RDSServer. DataFactory, consultez le bulletin de sécurité Microsoft MS99-025 sur le [site Web de sécurité de Microsoft](https://www.microsoft.com/en-us/security/default.aspx).

## <a name="client-impersonation-and-security"></a>Emprunt d'identité et sécurité client

Si la propriété **d'authentification de mot de passe** de votre serveur Web IIS est définie sur authentification par stimulation/réponse Windows NT (pour windows NT 4,0) ou sur authentification Windows intégrée (pour Windows 2000), les objets métier sont appelés sous le client contexte de sécurité. Il s'agit d'une nouvelle fonctionnalité de RDS 1.5 qui permet l'emprunt d'identité du client sur HTTP. Lorsque vous utilisez ce mode, la connexion au serveur Web (IIS) n'est pas anonyme, mais utilise l'ID d'utilisateur et le mot de passe sous lesquels l'ordinateur client est exécuté. Si les noms des sources de données ODBC sont configurés pour utiliser une connexion approuvée, l'accès aux bases de données, telles que SQL Server, s'opère également dans le contexte de sécurité du client. Mais cela fonctionne uniquement si la base de données réside sur le même ordinateur que Microsft IIS ; les informations d'identification du client ne peuvent pas être transférées sur un autre ordinateur.

Prenons l'exemple du client Jean Dupont, qui est connecté à un ordinateur client sous l'ID utilisateur « JeanD » et le mot de passe « secret ». Il utilise une application de type navigateur qui a besoin d'accéder à l'objet **RDSServer.DataFactory** pour créer un objet [Recordset](recordset-object-ado.md) en exécutant une requête SQL sur l'ordinateur « MonServeur » exécutant IIS. MonServeur, qui est un système fonctionnant sous Windows NT Server 4.0, est configuré pour utiliser l'Authentification par simulation/réponse de Windows NT, son nom de source de données ODBC est configuré pour utiliser une connexion approuvée, et il contient également la source de données SQL Server. Lorsqu'une demande est reçue sur le serveur Web, elle demande au client l'ID et le mot de passe de l'utilisateur. Par conséquent, la demande est consignée sur MyServer comme provenant de «JohnD»/«secret»\_au lieu de IUser MyServer (valeur par défaut lorsque l'authentification du mot de passe anonyme est activée). De la même manière, « JeanD »/« Secret » est utilisé pour se connecter à SQL Server.

Par conséquent, le mode d'authentification par stimulation/réponse de Windows NT permet la création de pages HTML sans que l'utilisateur soit explicitement invité à fournir l'ID utilisateur et le mot de passe nécessaires pour se connecter à la base de données. Si l'authentification de base IIS avait été utilisée, ces informations auraient aussi été nécessaires.

## <a name="password-authentication"></a>Authentification par mot de passe

RDS peut communiquer avec un serveur Web IIS s'exécutant dans l'un des trois modes d'authentification de mot de passe: anonyme, de base ou authentification par stimulation/réponse NT (appelée authentification Windows intégrée dans Windows 2000). Ces paramètres définissent la façon dont un serveur Web contrôle l'accès par le biais de celui-ci, par exemple pour exiger qu'un ordinateur client dispose de privilèges d'accès explicites sur le serveur Web NT.

