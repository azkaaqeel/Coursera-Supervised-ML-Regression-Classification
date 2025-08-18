### Define Models

Below are implementations for each specified classifier:

1. **Decision Tree**

    
    `dt_model = DecisionTreeClassifier(random_state=42) dt_model.fit(X_train, y_train) y_pred_proba = dt_model.predict_proba(X_val)[:, 1] print("Decision Tree ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    ``
    
2. **Naive Bayes**
    
    
    `nb_model = GaussianNB() nb_model.fit(X_train, y_train) y_pred_proba = nb_model.predict_proba(X_val)[:, 1] print("Naive Bayes ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    
3. **K-Nearest Neighbor (KNN)**

    
    `knn_model = KNeighborsClassifier(n_neighbors=5) knn_model.fit(X_train, y_train) y_pred_proba = knn_model.predict_proba(X_val)[:, 1] print("K-Nearest Neighbor ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    
4. **Random Forest**
    
    
    `rf_model = RandomForestClassifier(n_estimators=100, max_depth=8, random_state=42, n_jobs=-1) rf_model.fit(X_train, y_train) y_pred_proba = rf_model.predict_proba(X_val)[:, 1] print("Random Forest ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    
5. **Gradient Boosting**
    
    python
    
    Copy code
    
    `gb_model = GradientBoostingClassifier(n_estimators=100, random_state=42) gb_model.fit(X_train, y_train) y_pred_proba = gb_model.predict_proba(X_val)[:, 1] print("Gradient Boosting ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    
6. **Adaptive Boosting (AdaBoost)**
    
    python
    
    Copy code
    
    `ab_model = AdaBoostClassifier(n_estimators=100, random_state=42) ab_model.fit(X_train, y_train) y_pred_proba = ab_model.predict_proba(X_val)[:, 1] print("Adaptive Boosting ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    
7. **Light GBM**
    
    python
    
    Copy code
    
    `lgb_model = LGBMClassifier(n_estimators=100, random_state=42) lgb_model.fit(X_train, y_train) y_pred_proba = lgb_model.predict_proba(X_val)[:, 1] print("Light GBM ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    
8. **XGBoost**
    
    python
    
    Copy code
    
    `xgb_model = XGBClassifier(n_estimators=100, use_label_encoder=False, eval_metric='logloss', random_state=42) xgb_model.fit(X_train, y_train) y_pred_proba = xgb_model.predict_proba(X_val)[:, 1] print("XGBoost ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    
9. **CatBoost**
    
    python
    
    Copy code
    
    `cb_model = CatBoostClassifier(iterations=100, verbose=0, random_state=42) cb_model.fit(X_train, y_train) y_pred_proba = cb_model.predict_proba(X_val)[:, 1] print("CatBoost ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    
10. **BaggingClassifier**
    
    python
    
    Copy code
    
    `bag_model = BaggingClassifier(n_estimators=100, random_state=42) bag_model.fit(X_train, y_train) y_pred_proba = bag_model.predict_proba(X_val)[:, 1] print("Bagging Classifier ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    
11. **Extra Trees Classifier**
    
    python
    
    Copy code
    
    `et_model = ExtraTreesClassifier(n_estimators=100, random_state=42) et_model.fit(X_train, y_train) y_pred_proba = et_model.predict_proba(X_val)[:, 1] print("Extra Trees ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    
12. **Voting Classifier (Hard Voting)**
    
    python
    
    Copy code
    
    `from sklearn.ensemble import VotingClassifier voting_model = VotingClassifier(     estimators=[('rf', rf_model), ('gb', gb_model), ('xgb', xgb_model)],     voting='soft' ) voting_model.fit(X_train, y_train) y_pred_proba = voting_model.predict_proba(X_val)[:, 1] print("Voting Classifier ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    
13. **Stacking Classifier**
    
    python
    
    Copy code
    
    `from sklearn.ensemble import StackingClassifier stacking_model = StackingClassifier(     estimators=[('rf', rf_model), ('gb', gb_model), ('xgb', xgb_model)],     final_estimator=LogisticRegression() ) stacking_model.fit(X_train, y_train) y_pred_proba = stacking_model.predict_proba(X_val)[:, 1] print("Stacking Classifier ROC AUC:", roc_auc_score(y_val, y_pred_proba))`
    

Each model trains on the processed data with SMOTE applied, and the ROC AUC score is printed for comparison. You can save or further process the best-performing model’s predictions for your final submission.


