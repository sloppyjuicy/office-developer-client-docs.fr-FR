---
title: Initialisation du fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 977c18ce-ece5-4ad1-ac97-5a680846ab83
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3b369e20101bbaba5e246b2ef9f6ab3ed1771ef6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563554"
---
# <a name="initializing-the-transport-provider"></a>Initialisation du fournisseur de transport

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
L’interface de transport-spouleur définit le spouleur MAPI appels à un fournisseur de transport. Fournisseurs de transport implémentent ces routines dans une bibliothèque de liens dynamiques (DLL). Premier point d’entrée directe dans la DLL utilisé par le spouleur MAPI doit être la fonction d’initialisation du fournisseur transport [XPProviderInit](xpproviderinit.md).
  
MAPI utilise la routine **GetProcAddress** pour obtenir l’adresse de la routine d’initialisation du fournisseur de services, puis appelle cette routine. Le nom de la routine d’initialisation est **XPProviderInit** pour les fournisseurs de transport. Il est différent pour les autres types de fournisseurs de services MAPI afin qu’une DLL peut contenir n’importe quelle combinaison de types de fournisseur de service, mais uniquement seul fournisseur de services d’un type particulier. Toutefois, un fournisseur de services d’un type donné peut implémenter plusieurs services de son type. Par exemple, un fournisseur de transport peut implémenter la fonctionnalité transport message à plusieurs services de messagerie. 
  
Le fichier d’en-tête mapispi.h a une définition de type pour le prototype de fonction de la fonction de l’initialisation de fournisseur de transport et un nom de procédure prédéfinis pour celui-ci. Déclaration de votre DLL d’exportation en le nommant les routines d’initialisation dans vos fichiers C et C++ portant le même nom que celui utilisé par **GetProcAddress** et à l’aide d’un simple. Fichier de définition, vous obtenez automatiquement la vérification des paramètres de votre routine d’initialisation de type. Voir l’exemple transport fournisseur de code source pour obtenir des exemples. Pour plus d’informations, voir [Exemple de fournisseur de Transport](transport-provider-sample.md).
  
Si appel de l’initialisation d’un fournisseur de services réussit, mais cette propriété renvoie un fournisseur de services de numéro de version d’interface trop petit pour MAPI gérer, MAPI immédiatement appelle la méthode de **publication** de l’objet de fournisseur de service et procède comme si l’appel de l’initialisation a échoué avec MAPI_E_VERSION. De cette manière MAPI et le fournisseur de services conjointement définissent la plage de numéros de version interface fournisseur service qu'ils peuvent gérer, et si rien correspond au chargement de fournisseur de services échoue avec une MAPI_E_VERSION renvoie la valeur. 
  
Pour le spouleur MAPI dans l’accès à des ressources du service fournisseur de la dernière étape consiste à ouvrir une session sur le fournisseur de transport. Le spouleur MAPI appelle la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) de la [IXPProvider : IUnknown](ixpprovideriunknown.md) objet renvoyé à partir de **XPProviderInit**. Il s’agit de l’appel où les informations d’identification, en cas d’utilisation, et affiche les boîtes de dialogue peuvent être autorisés.
  
Si un processus s’ouvre une deuxième session de transport sur le même fournisseur de transport et de la session MAPI, la DLL du fournisseur de transport ne doit pas créer un second objet de fournisseur. Le premier objet fournisseur doit être utilisé pour vous connecter à la deuxième session de transport. Un fournisseur de transport doit être programmé pour prendre en charge plusieurs sessions de transport dans un objet de fournisseur unique. Un deuxième objet fournisseur doit être créé uniquement si les sessions MAPI différentes sont utilisées dans le même processus.
  

