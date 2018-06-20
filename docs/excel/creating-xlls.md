---
title: Création de XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- DLL [excel 2007], appel dans excel, fonction xlAutoFree [Excel 2007], fonction xlAutoFree12 [2007],xlcall32.lib Excel [Excel 2007], fonction xlAutoRegister [2007],xlcall.cpp Excel [Excel 2007], fonction xlAutoRemove [Excel 2007], xlAddInManagerInfo fonction [Excel 2007], xlAutoAdd, fonction [Excel 2007], fonction xlAutoOpen [Excel 2007], xlAutoClose fonction [Excel 2007], [Excel 2007], les DLL transformer en XLL, XLL [Excel 2007], appel dans Excel, la fonction xlAutoRegister12 [Excel 2007],xlcall.h [Excel 2007], xlAddInManagerInfo12, fonction [Excel 2007]
localization_priority: Normal
ms.assetid: 7754998f-4e13-4a37-9724-43b6ee6c919b
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: de347d34768c25adf0d96642b4fade781ae26a9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782027"
---
# <a name="creating-xlls"></a>Création de XLL

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Si votre DLL est autonome ou s’appuie uniquement sur les autres bibliothèques, vous devez savoir comment permettent à Microsoft Excel accéder aux fonctions et les commandes. Pour plus d’informations, consultez [Accès aux DLL dans Excel](how-to-access-dlls-in-excel.md). 
  
Toutefois, si votre DLL doit accéder aux fonctionnalités d’Excel (par exemple, pour obtenir le contenu d’une cellule, pour appeler une fonction de feuille de calcul ou interroger Excel pour obtenir des informations d’espace de travail), votre code doit être en mesure d’effectuer un rappel dans Excel.
  
L’API C Excel offre plusieurs fonctions permettant de DLL vers Excel. Pour accéder à ces, la DLL doit être liée statiquement au moment de la compilation avec la bibliothèque Excel 32 bits, xlcall32.lib. La bibliothèque statique est téléchargeable à partir de Microsoft en tant que partie de Microsoft Excel 2013 XLL SDK, qui inclut les versions 32 bits et 64 bits de cette bibliothèque.
  
## <a name="enabling-dlls-to-call-back-into-excel"></a>Activation de la DLL à l’appel dans Excel

Pour être en mesure d’accéder aux fonctionnalités dans Excel et obtenir ou définir une DLL informations d’espace de travail, il doit d’abord obtenir les adresses des fonctions de rappel Excel **Excel4**, **Excel4v**, **Excel12**et **Excel12v**. Les deux dernières ont été introduits dans Excel 2007 et sont disponibles dans les versions ultérieures. Pour accéder à toutes ces, le projet de DLL doit inclure les références pour les fichiers suivants à partir du Kit de développement logiciel XLL Excel 2013. Si vous souhaitez accéder uniquement les deux premières rappels (dans n’importe quelle version de Microsoft Excel), votre projet doit inclure uniquement les deux premiers fichiers.
  
### <a name="xlcallh"></a>Xlcall.h

Le fichier Xlcall.h contient les éléments suivants :
  
- Prototypes de fonction pour toutes les fonctions de rappel.
    
- Définitions des structures de données qui utilisent des rappels pour échanger des données entre les DLL/XLL Excel et les définitions de constantes de type de données.
    
- Définitions des équivalents fonction et commandes API C de la feuille de calcul, fonctions de feuille macro, commandes Excel prises en charge.
    
- Valeurs de retour de définitions de fonction de rappel.
    
Vous devez utiliser le **#include** directive pour ce fichier, directement ou indirectement via un autre fichier d’en-tête, tous les fichiers qui accèdent à l’API C ou pour gérer les types de données qui utilise l’API C. 
  
### <a name="xlcall32lib"></a>Xlcall32.lib

La bibliothèque Xlcall32.lib exporte les deux premières rappels **Excel4** et **Excel4v**et également la fonction **XlCallVer** . Sans une référence à cette bibliothèque dans votre projet, l’éditeur de liens ne peut pas créer la ressource XLL si vous avez utilisé une de ces rappels dans votre code. (Vous pouvez obtenir les adresses de ces fonctions par une liaison dynamique à l’équivalent Xlcall32.dll qui est copié dans votre système dans le cadre d’une installation Excel normale). 
  
### <a name="xlcallcpp"></a>Xlcall.cpp

Les rappels Excel **Excel12** et **Excel12v** ne sont pas exportés dans Xlcall32.lib. Cela garantit que les projets XLL que vous créez à compter d’Excel 2007 fonctionne également avec les versions antérieures d’Excel. Le module Xlcall.cpp contient le code pour **Excel12** et **Excel12v** fonctions qui appellent une entrée Excel point à compter d’Excel 2007 ou de renvoient une valeur d’erreur de sécurité si vous exécutez une version antérieure de Microsoft Excel. Si vous souhaitez créer une solution XLL qui s’exécute à compter d’Excel 2007 et qui est en mesure d’utiliser les nouveaux types de données qui prennent en charge grilles plus grandes et plus chaînes Unicode, vous devez inclure ce module dans votre projet. 
  
> [!NOTE]
> Commencer avec le Kit de développement Excel 2010, ce fichier peut être compilé pour XLL 32 bits et 64 bits. 
  
## <a name="turning-dlls-into-xlls-add-in-manager-interface-functions"></a>La DLL en XLL : Gestionnaire de fonctions de l’Interface du complément

Une solution XLL est une DLL qui exporte plusieurs procédures qui sont appelées par Excel ou le Gestionnaire de compléments Excel. Ces procédures sont décrites brièvement ici et décrit en détail dans le [Gestionnaire de compléments et les fonctions de l’Interface XLL](add-in-manager-and-xll-interface-functions.md). Tous ces rappels DLL commencent par le préfixe **xlAuto**. Seule une d'entre eux, la commande **xlAutoOpen**, est requise. Elle est appelée lorsque le complément est activé, et il est généralement utilisé pour enregistrer les fonctions XLL dans Excel et d’autres tâches d’initialisation des commandes. Exemples d’implémentation de toutes les fonctions **xlAuto** les signatures de fonction sont fournies dans les sections suivantes. 
  
Même si **xlAutoOpen** est le seul requis de ces rappels, votre complément deviez également exporter d’autres personnes en fonction de son comportement. 
  
Excel 2007 introduit un nouveau type de données, **XLOPER12**, pour prendre en charge les grilles plus grandes et pour prendre en charge les chaînes Unicode longues. **XLOPER12** est décrit plus loin dans cette rubrique. Tandis que les fonctions **xlAuto** prendront ou renvoient le type de données ancien **XLOPER**, les nouvelles versions de ces fonctions ont été introduites dans Excel 2007 qui utilisent des types de données **XLOPER12** . À l’exception de **xlAutoFree12**, que vous devez parfois implémenter pour éviter la mémoire **XLOPER12** fuites, vous pouvez omettre en toute sécurité de toutes les version 12 **xlAuto** fonctions, dans ce cas, à compter d’Excel 2007, les appels le **XLOPER** Excel versions. 
  
### <a name="xlautoopen"></a>xlAutoOpen

Excel appelle la fonction [xlAutoOpen](xlautoopen.md) chaque fois que la ressource XLL est activée. Le complément sera activé au début d’une session Excel si elle a été actif dans la dernière session Excel qui s’est terminée normalement. Le complément est activé s’il est chargé pendant une session d’Excel. Le complément peut être désactivé et réactivé pendant une session de Excel et la fonction est appelée sur réactivation. 
  
Vous devez utiliser **xlAutoOpen** pour enregistrer les commandes et les fonctions XLL, initialiser les structures de données, personnaliser l’interface utilisateur et ainsi de suite. 
  
Si votre complément implémente et exporte la fonction [xlAutoRegister](xlautoregister-xlautoregister12.md) ou [xlAutoRegister12](xlautoregister-xlautoregister12.md) , Excel peut tenter d’activer et enregistrer une fonction ou une commande sans appeler d’abord la fonction **xlAutoOpen** . Dans ce cas, vous devez vous assurer que votre complément est suffisamment initialisé pour votre fonction ou la commande fonctionne correctement. S’il n’est pas le cas, vous défaillance soit la tentative d’inscrire la fonction ou la commande ou d’effectuer l’initialisation nécessaire. 
  
### <a name="xlautoclose"></a>xlAutoClose

Excel appelle la fonction [xlAutoClose](xlautoclose.md) chaque fois que la ressource XLL est désactivée. Le complément sera désactivé quand une session Excel se termine normalement. Si l’utilisateur désactive le complément pendant une session Excel, la fonction est appelée. 
  
Vous devez utiliser **xlAutoClose** pour annuler l’inscription des fonctions et les commandes, libérer des ressources, annuler des personnalisations et ainsi de suite. 
  
> [!NOTE]
> Il existe un problème connu avec l’annulation de l’inscription des fonctions et des commandes. Pour plus d�informations, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md). 
  
### <a name="xlautoadd"></a>xlAutoAdd

Excel appelle la [fonction xlAutoAdd](xlautoadd.md) dès que l’utilisateur a activé la XLL pendant une session Excel à l’aide du Gestionnaire de compléments. Cette fonction n’est pas appelée lorsque Excel démarre et charge un complément préinstallé. 
  
Vous pouvez utiliser cette fonction pour afficher une boîte de dialogue personnalisée qui indique à l’utilisateur que le complément a été activé pour lire ou écrire dans le Registre ou pour vérifier les informations de licence.
  
### <a name="xlautoremove"></a>xlAutoRemove

Excel appelle la fonction [xlAutoRemove](xlautoremove.md) chaque fois que l’utilisateur désactive le XLL pendant une session Excel à l’aide du Gestionnaire de compléments. Cette fonction n’est pas appelée lorsqu’une session Excel se ferme, normale ou anormale, avec le complément installé. 
  
Vous pouvez utiliser cette fonction pour afficher une boîte de dialogue personnalisée qui indique à l’utilisateur que le complément a été désactivé, ou pour lire ou écrire dans le Registre.
  
### <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

Excel appelle la fonction [xlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md) lorsque le Gestionnaire de compléments est appelé pour la première fois dans une session d’Excel. Si Excel passe un argument est égale à 1, cette fonction doit renvoyer une chaîne (en règle générale, le nom de la macro complémentaire) ; Sinon, elle doit retourner **#VALUE !**.
  
À compter d’Excel 2007, Excel appelle la fonction **xlAddInManagerInfo12** plutôt que la fonction **xlAddInManagerInfo** , si elle est exportée par la ressource XLL. La fonction **xlAddInManagerInfo12** devrait fonctionner de la même manière que la fonction **xlAddInManagerInfo** pour éviter les différences spécifiques à la version de comportement de la ressource XLL. La fonction **xlAddInManagerInfo12** doit renvoyer un type de données **XLOPER12** , tandis que la fonction **xlAddInManagerInfo** doit renvoyer un type de données **XLOPER** . 
  
### <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

Excel appelle la fonction [xlAutoRegister](xlautoregister-xlautoregister12.md) chaque fois qu’un appel a été effectué pour la fonction XLM **inscrire**ou la fonction équivalente [xlfRegister](xlfregister-form-1.md) API C, avec le retour et types d’arguments manquante pour la fonction en cours d’enregistrement. La fonction **xlAutoRegister** permet la ressource XLL à rechercher ses listes internes de fonctions exportées et commandes pour enregistrer la fonction avec l’argument et renvoyer les types spécifiés. 
  
À compter d’Excel 2007, Excel appelle la fonction **xlAddInRegister12** plutôt que la fonction **xlAddInRegister** , si elle est exportée par la ressource XLL. 
  
> [!NOTE]
> Si **xlAddInRegister**/ **xlAddInRegister12** tente d’inscrire la fonction sans fournir l’argument et retournent des types, une récursive appelant boucle se produit et finalement de dépassement de la pile des appels et obliger Excel à fermer ou arrêter répondre. 
  
### <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

Excel appelle la fonction [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md) juste après qu’une fonction de feuille de calcul XLL renvoie un **XLOPER**/ des types de données**XLOPER12** avec un indicateur qui indique à Excel de mémoire que la XLL doit toujours libérer. Cela permet à la ressource XLL à renvoyer allouées dynamiquement des tableaux, des chaînes et des références externes de la feuille de calcul sans fuites de mémoire. À compter d’Excel 2007, le type de données **XLOPER12** est pris en charge. Pour plus d�informations, voir [Gestion de la m�moire dans Excel](memory-management-in-excel.md).
  
> [!NOTE]
> À compter d’Excel 2007, lorsque Excel est configuré pour utiliser le recalcul de la feuille de calcul multithread, le **xlAutoFree**/ fonction**xlAutoFree12** est appelée sur le même thread qui a été utilisé seulement pour appeler la fonction qui a renvoyé. L’appel à **xlAutoFree**/ **xlAutoFree12** est toujours effectuées avant l’évaluation des cellules de la feuille de calcul suivantes sur ce thread. Cela simplifie la création de thread-safe dans votre XLL. Pour plus d’informations, voir [Multithread le recalcul dans Excel](multithreaded-recalculation-in-excel.md). 
  
### <a name="creating-64-bit-xlls"></a>Création de XLL 64 bits

Excel et les fonctions définies par l’utilisateur peuvent exécuter sur les systèmes d’exploitation 64 bits pour tirer parti des avantages de performances sur les systèmes d’exploitation 32 bits. Excel passe des valeurs dans des structures **XLOPER12** qui incluent des informations sur les types de données. Soyez prudent lors de la conversion entre types natifs comme **int** ou pointeurs pour conserver les valeurs du type supérieure et les valeurs dans la structure **XLOPER12** . 
  
## <a name="see-also"></a>Voir aussi



[Appel des fonctions XLL à partir de l’Assistant fonction ou remplacer des boîtes de dialogue](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
[Gestionnaire de compléments et les fonctions de l’Interface XLL](add-in-manager-and-xll-interface-functions.md)
  
[D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)

