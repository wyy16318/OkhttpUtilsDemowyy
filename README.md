# OkhttpUtilsDemowyy
基于鸿洋大神okhttputils封装的返回回调gson解析

 private void getData() {
        OkHttpUtils
                .get()
                .url("http://gank.io/api/history/content/day/2016/05/11")
                .build()
                .execute(new ResponseCallback<ResultData<ResultBean1>>(){
                    @Override
                    public void onResponse(ResultData<ResultBean1> response, int id) {
                        Log.i("wyy", "onResponse: -----"+response.getResults().toString());
                        if (!response.error) {
                            tv_date.setText( response.getResults().get(0).get_id());
                        }
                    }
                });
    }

